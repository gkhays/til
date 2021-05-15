# Open a New Tab or Window from Form

Add a target directive to the form.

```html
<form action="#" method="post" target="_blank">...</form>
```

This alternative looked interesting enough to write down.

```html
<form name="testform" method="post">
  <input type="text" name="name" value="test" />
  <input
    type="submit"
    value="Submit"
    onclick="this.form.target='_blank';return true;"
  />
</form>
```

I knew this one already.

```html
<a href="#" target="_blank">link</a>
```

## References

1. [Form Submission Opens New Tab/Window](https://css-tricks.com/snippets/html/form-submission-new-window/)
1. [Submitting form to a new window](https://www.plus2net.com/html_tutorial/submit-new.php)
