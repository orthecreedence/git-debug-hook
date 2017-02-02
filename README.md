# What does this do?

This is a pre-commit hook you put in your git repo.

It allows you to write comments in your code like this:

```javascript
// DEBUG: remove this log
console.log('some debug stuff: ', debug_val);
```

When you try to commit this file, it bitches at you, saying:

```
Please address the DEBUG comments in following files before committing:

  user.js
```

Boom! You can't commit the file until you remove the DEBUG comment, which is a
great reminder to not commit your debug code.

# Usage

Simply put the file `pre-commit.debug-comments` into `.git/hooks/pre-commit`.
You can also host this repo somewhere else and symlink `.git/hooks/pre-commit`
to `git-debug-hook/pre-commit.debug-comments`.

That's it!

# Supported languages

The hook detects language by file extension (ie, .js -> javascript, .lisp ->
lisp, etc).

- javascript
- rust
- html
- lisp
- (ba)sh
- handlebars

# Contributing

If you want support for a certain language, don't open an issue, I'll probably
just ignore it (being realistic here).

Fork the project and open a pull request. Be sure to also add your language to
the [supported language list](#supported-languages) or I'll contact the
authorities. GOOD DAY, SIR/MADAM/NON-GENDER-CONFORMING-FORMAL-TITLE.

# License

MIT. Yay.

