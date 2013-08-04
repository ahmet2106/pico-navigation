# Pico Navigation Plugin

This is a Plugin for the Flat File Based CMS named [Pico](pico.dev7studios.com/).

## use

Copy the `at_navigation.php` File to the `plugins` Folder in the Root of your Pico Project. Every Plugin in this Folder is activated automatically.

In your **theme** you only have to add this line where your navigation should be:

    {{ at_navigation.navigation }}

I redesigned the style of the **default theme** for a quick preview. The output is like this:

![Default Theme with at_navigation Plugin](img.png)


### set id and class of navigation element

Add these two lines to your `config.php` to change **id** and/ or **class** from `at-navigation` to anything you want:

```
$config['at_navigation']['id'] = 'at-navigation';
$config['at_navigation']['class'] = 'at-navigation';
```

### exclude pages and folders
Add these two lines to your `config.php` to exclude **single pages** and/ or **folders**:

```
$config['at_navigation']['exclude']['single'] = array('a/site', 'another/site');
$config['at_navigation']['exclude']['folder'] = array('a/folder', 'another/folder');
```

## what it does

This Plugin generates a better navigation with child navigations and editable configuration.

So the output looks like:

    <ul id="at-navigation" class="at-navigation">
        <li><a href="…" title="…">…</a></li>
        <li>
            <a href="…" title="…">…</a>
            <ul>
                <li class="is-active"><a href="#" class="is-active" title="…">…</a></li>
            </ul>
        </li>
    </ul>

As you can see it will add an `.is-active` class to the `<a>` and `<li>` element of the **active page**.


## licence

CreativeCommons2.0 licence: [CC BY-SA](http://creativecommons.org/licenses/by-sa/2.0/)

You are free to share & remix this code only if you mention me as coder of this base.


## copyright

**Copyright © Ahmet Topal 2013. All rights reserved.**