---
title: Simple Listbox Ordering using a CollectionViewSource
gist: d7c30aac470af4900cb5
links:
- ["CollectionViewSource is crazy useful for binding to filtered Observable Collections on Windows Phone 8",http://www.hanselman.com/blog/collectionviewsource-is-crazy-useful-for-binding-to-filtered-observable-collections-on-windows-phone-8]
- ["Stack Overflow: How can I sort a ListBox using only XAML and no code-behind?",http://stackoverflow.com/questions/1280704/how-can-i-sort-a-listbox-using-only-xaml-and-no-code-behind)
tags: 
- XAML
---
As with most xaml based apps there are any number of ways of ordering a list of items. A quick and straightforward way to do this entirely in xaml is to use a [CollectionViewSource](https://msdn.microsoft.com/en-us/library/system.windows.data.collectionviewsource(v=vs.110).aspx).

This example will order a bound list 'List' based on the listed object's 'Name' property. 

The [SortDescription](https://msdn.microsoft.com/en-us/library/system.componentmodel.sortdescription(v=vs.110).aspx) binding is clever enough to raise an error if the property selected doesn't implement [IComparable](https://msdn.microsoft.com/en-us/library/system.icomparable(v=vs.110).aspx).
