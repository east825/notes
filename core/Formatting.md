Formatting
==========

Code style settings
-------------------

* `CodeStyleSettingsManager.getSettings(project).getCommonSettins(lang)` -
get common settings for the language `lang`

* `CodeStyleSettingsManager.getSettings(project).getCusomSettings(cls)` -
get custom settings represented as instance of bean class `cls`

* `CodeStyleSettingsManager.getSettings(myFixture.getProject()).getRightMargin(lang)` -
get language-specifc right margin

Advanced formatting
-------------------

### Disable automatic reformat

Normally reformat is performed automatically on every modification of PSI tree.
E.g. if you insert new child of PSI element, its surrounding whitespaces is
adjusted automatically according to your code style settings. However sometimes
such "smart" behavior is not desirable. In this case you can temporarily disable
it using `CodeStyleManager#performActionWithFormatterDisabled`.
