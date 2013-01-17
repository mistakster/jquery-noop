# The smallest jQuery plugin ever

[Описание плагина по-русски](http://noteskeeper.ru/381/)

## Overview

The simplest and smallest plugin will only consist of a single expression `return this`.

	$.fn.noop = function () {
		return this;
	};

Utility of this plugin is not obvious at first glance. If you call it as usual,
the result will be the same unmodified collection of items.

	$("div.title").noop().doSomething();

The practical benefit of it will be when the plug-in should be called implicitly.

	$("div.title")[isVisible() ? "fadeTo" : "noop"](333, 0).doSomething();

In some cases this notation is useful when you don't need to save the results of query in a variable.
In a particular example is fairly natural chaining of several actions on items.

## Note

This plugin was inspired by [Artyom Polikarpov](https://github.com/artpolikarpov)'s
[tweet](https://twitter.com/artpolikarpov/statuses/159653096606273536).

## License

This plugin is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).
