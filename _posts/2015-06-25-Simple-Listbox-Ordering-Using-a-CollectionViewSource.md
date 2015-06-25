---
layout: post
title: Simple Listbox Ordering using a CollectionViewSource
tags: [xaml]
---
As with most xaml based apps there are any number of ways of ordering a list of items. A quick and straightforward way to do this entirely in xaml is to use a [CollectionViewSource](https://msdn.microsoft.com/en-us/library/system.windows.data.collectionviewsource(v=vs.110).aspx).

{% gist d7c30aac470af4900cb5 %}

The above example will order a bound list 'List' based on the listed object's 'Name' property. 

See also this [example](http://www.hanselman.com/blog/CollectionViewSourceIsCrazyUsefulForBindingToFilteredObservableCollectionsOnWindowsPhone8.aspx) by [Scott Hanselman](http://www.hanselman.com).
