---
layout: post
tags: [c# dropbox]
---
The Dropbox folder path is stored in host.db in the Dropbox ApplicationData folder.

[Stack Overflow: How do I programmatically locate my Dropbox folder using C#?](http://stackoverflow.com/questions/9660280/)

[Gist](https://gist.github.com/idiotandrobot/67a630abfef6097fe93d)

{% highlight c# %}
 using System;
 using System.IO;
 using System.Text;
 
 public static class Dropbox
 {
   private static string _Path;
   public static string Path
   {
       get { return _Path ?? (_Path = GetPath()); }
   }
 
   static string GetPath()
   {
       var appDataPath = Environment.GetFolderPath(
                                      Environment.SpecialFolder.ApplicationData);
       var dbPath = System.IO.Path.Combine(appDataPath, "Dropbox\\host.db");
 
       var lines = File.ReadAllLines(dbPath);
       var dbBase64Text = Convert.FromBase64String(lines[1]);
       var folderPath = Encoding.UTF8.GetString(dbBase64Text);
 
       return folderPath;
   }
 }
{% endhighlight %}
