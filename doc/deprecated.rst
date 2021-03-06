Deprecated Features
===================

This document lists deprecated features in Twig 2.x. Deprecated features are
kept for backward compatibility and removed in the next major release (a
feature that was deprecated in Twig 2.x is removed in Twig 3.0).

Inheritance
-----------

* Defining a "block" definition in a non-capturing block in a child template is
  deprecated since Twig 2.5.0. In Twig 3.0, it will throw a
  ``Twig\Error\SyntaxError`` exception. It does not work anyway, so most
  projects won't need to do anything to upgrade.

Errors
------

 * Passing a string as the ``$source`` argument on ``\Twig\Error\Error`` /
   ``Twig\Error\Error`` constructor is deprecated since Twig 2.6.1. Pass an
   instance of ``Twig\Source`` instead.

Tags
----

* Using the ``spaceless`` tag at the root level of a child template is
  deprecated in Twig 2.5.0. This does not work as one would expect it to work
  anyway. In Twig 3.0, it will throw a ``Twig\Error\SyntaxError`` exception.

Final Classes
-------------

The following classes are marked as ``@final`` in Twig 2 and will be final in
3.0:

* ``Twig\Node\ModuleNode``
* ``Twig\TwigFilter``
* ``Twig\TwigFunction``
* ``Twig\TwigTest``
* ``Twig\Profiler\Profile``

Parser
------

* As of Twig 2.7, the ``\Twig\Parser::isReservedMacroName()`` / ``Twig\Parser``
  function is deprecated and will be removed in Twig 3.0. It always returns
  ``false`` anyway as Twig 2 does not have any reserved macro names.

Environment
-----------

* As of Twig 2.7, the ``base_template_class`` option on ``Twig\Environment`` is
  deprecated and will be removed in Twig 3.0.

* As of Twig 2.7, the ``Twig\Environment::getBaseTemplateClass()`` and
  ``Twig\Environment::setBaseTemplateClass()`` methods are deprecated and will
  be removed in Twig 3.0.
