# The smallest jQuery plugin ever

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
In a particular example is fairly natural association of several actions on items in chain.

# The original idea

This plugin was inspired by [Artyom Polikarpov](https://github.com/artpolikarpov)'s
[tweet](https://twitter.com/artpolikarpov/statuses/159653096606273536).

# Самый маленький плагин для jQuery

Простейший плагин будет состоять только из одного выражения `return this`.

	$.fn.noop = function () {
		return this;
	};

Профит от этого плагина не очевиден на первый взгляд. Если вызвать его, как вызываются тысячи других,
то в результате получим ту же самую не модифицированную коллекцию элементов.

	$("div.title").noop().doSomething();

Практическая польза от него будет, когда плагин должен вызываться неявно.

	$("div.title")[isVisible() ? "fadeTo" : "noop"](333, 0).doSomething();

В некоторых случаях такую нотацию удобно использовать, когда не требуется специально сохранять результаты
выборки элементов в отдельную переменную. В конкретном примере достаточно естественного объединения нескольких
действий над элементами в цепочку.

# Оригинальная идея

Плагин сделан под вдохновением от [твита](https://twitter.com/artpolikarpov/statuses/159653096606273536)
[Артёма Поликарпова](https://github.com/artpolikarpov).

# Страница проекта

http://noteskeeper.ru/381/
