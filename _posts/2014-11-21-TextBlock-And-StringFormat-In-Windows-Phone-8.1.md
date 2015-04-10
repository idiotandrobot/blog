---
layout: post
title: TextBlock StringFormat Support in Windows Phone 8.1 Projects
tags: [wp81 xaml]
redirect_from:
 - /:year/:month/:day/:title/
---
In trying to create a custom control for a Windows Phone 8.1 project I was having an odd problem where StringFormat didn't seem to be supported by the TextBlock control Text property any more so the following style raised an error against `StringFormat=T`: 

{% highlight c# %}
<Style TargetType="controls:Clock">
<Setter Property="Template">
<Setter.Value>
<ControlTemplate TargetType="controls:Clock">
<TextBlock Text="{Binding DateTime, 
StringFormat=T,
RelativeSource={RelativeSource TemplatedParent}}" />
</ControlTemplate>
</Setter.Value>
</Setter>
</Style>
{% endhighlight %}

This was odd as the page was already covered in xaml like this:


		<TextBlock Text="{Binding Minutes, StringFormat='00'}" />

		<TextBlock Text="{Binding Seconds, StringFormat='00'}" /> 


Which displayed (the integer values Minutes and Seconds) formatted to two digits as you'd expect.

A couple of [StackOverflow](http://stackoverflow.com/) questions seemed to confirm that StringFormat isn't supported (anymore):

- [StringFormat in XAML](http://stackoverflow.com/questions/24966425/stringformat-in-xaml)
- [Windows Phone 8.1 XAML StringFormat](http://stackoverflow.com/questions/24127262/windows-phone-8-1-xaml-stringformat)

And that the lack of support seems to be dependant on the type of project (i.e. WinRT doesn't support StringFormat so neither do Universal App projects).

Both of those questions have answers that suggest using a converter instead:

**StringFormatConverter**

C# 

		public sealed class StringFormatConverter : IValueConverter
		{
		    public object Convert(object value, Type targetType, object parameter, string language)
		    {
		        if (value == null)
		            return null;
		
		        if (parameter == null)
		            return value;
		
		        return string.Format((string)parameter, value);
		    }
		
		    public object ConvertBack(object value, Type targetType, object parameter,
		        string language)
		    {
		        throw new NotImplementedException();
		    }
		}

XAML Fragments

		<StringFormatConverter x:Name="StringFormat"/>	
	
		<TextBlock Text="{Binding DateTime, StringFormat=T,	RelativeSource={RelativeSource TemplatedParent}}" />

This would also work but in the process of writing this post the original Clock style started working so I'm assuming something else I was doing in the custom control was at fault.

In summary StringFormat does seem to be supported still but if you get this error and need get it working quickly then either use an IValueConverter to get around the problem or write a blog post and that'll fix it.
