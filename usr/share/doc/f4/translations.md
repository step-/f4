# Translations

English is f4's main language.  The community freely provides translations to other languages.  Available translations are included in the release package.

## Call for translators

Translators will be credited for their contribution with a citation on the project repository pages.  Gettext-ready translations are preferred. If you do not know gettext, a simpler text-only translation will be accepted to incentivize contributions.

### Gettext-ready translation (I know gettext)

This is the recommended way to provide translations.
Please translate a copy of the `pot` template installed as `/usr/share/doc/nls/f4.pot`
([latest online main version](https://github.com/step-/f4/blob/master/usr/share/doc/nls/f4/f4.pot)).

**Note:** Generating a `po` file using PoEdit and other similar tools will not work correctly!  Translate a copy of the provided `pot` file.

### Text-only translation (I do not know gettext)

To incentivize enthusiastic translators who cannot prepare gettext-ready translations, the following text-only alternative is provided.

* Make a copy of `/usr/bin/f4`.
* You will test your translation by running your copy of f4.
* Edit your copy and find the line that starts with `i18n_table() {`; read the notes for translators above that line.
* Scroll to find the section that starts with this line:

```sh
$(gettext -es -- \
```

and ends with:

```sh
)
EOF
```

You want to translate the messages contained in this section. Replace the English text with text in your language making sure not to change the special codes in these strings otherwise your translation will not work correctly or your copy of f4 could not start.  If you make a mistake that freezes your copy of f4 just undo one or more steps of your translation until your copy of f4 can start again.

Test your copy frequently to minimize having to undo your work to retrace your steps.  When the translation is finished submit the whole translated section, including the enclosing lines, as explained further down.  The checklist refers to this submittal as the `i18n_table` attachment.

## Testing your translation

Whether your translation is gettext-ready or text-only, test it by exercising all possible functions of f4:

* window title
* the main terminal interface (typing prompt, hotkey summary)
* the help pager interface invoked with `Control-H` (typing prompt, hotkey summary)
* the Advanced settings expander invoked with `F1` (checkbox labels and tooltips, button labels and tooltips)
* the browser folder dialog invoked with `F2` (window title)
* the keep-out paths dialog invoked with `F3` (window title, inside text)
* the keep-out file systems dialog (window title, inside text)
* test all the hotkeys listed in section [Keyboard actions](keyboard-actions.md)

## Submitting a translation

Please submit **both** `po` and `mo` [files](https://www.gnu.org/software/gettext/manual/html_node/Files.html#Files) for your translation. Submitting just one file will force me to spend more time to add your translation to the project.

When you submit your files please state if and how you would like to be cited when your contribution is credited, e.g., one or more of your full name, e-mail, forum handle, website URL or none/anonymous (default).

When you make your submission you are implicitly accepting the license terms: you release your translation under the same [license terms of the f4 project](https://github.com/step-/f4/blob/master/LICENSE.md).

Submit your contributions as attachments to a new [github issue](https://github.com/step-/f4/issues) (requires a github account) or to the forum thread listed at the end of the [README](https://github.com/step-/f4/blob/master/README.md) file.

## SUBMISSION CHECKLIST

[ ] Which `LANG` code is your translation for? (`ll_CC`) ¹  
[ ] Which f4 version is this translation for? (x.x.x)  
[ ] «I tested this translation with f4 version x.x.x»  
[ ] Credit: one or more of full name, e-mail, forum handle, website URL or none/anonymous (default)  
[ ] License: «I release this translation under the same [license terms of the f4 project](https://github.com/step-/f4/blob/master/LICENSE.md)»  
[ ] Attach to a new github issue or forum thread post  
[ ] `po` file attached  
[ ] `mo` file attached  
[ ] `i18n_table` file attached  

Thank you!

¹ **Determining the `LANG` code**  
This code is the two- or three-letter lowercase abbreviation of the language followed by an underscore character followed by the two-letter uppercase abbreviation of the country code, eg. `en_US` for American English (see the first bullet list in [this answer](https://unix.stackexchange.com/a/149129)).  To determine this code try running the following command in a terminal *on the system in which f4 displays the translation correctly*:

```sh
echo $LANG`
```

----

[index](index.md)

