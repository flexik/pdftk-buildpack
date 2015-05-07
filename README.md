PDFtk Buildpack
----------------

# Purpose and Usage

Adds `pdftk` to `/app/vendor/pdftk`.

If you're using this, you need to add `pdftk` to your path.

```bash
heroku config
```

This will get you a list of environment variables on Heroku.

Look for the `PATH` variable and copy the part after the `PATH=` to your
clipboard.

Run the command below replacing `YOUR_EXISTING_PATH` with what you
copied to your clipboard.

```bash
heroku config set PATH=/app/vendor/pdftk/bin:YOUR_EXISTING_PATH
```

If you're using the C bindings, you'll need to modify `LD_LOAD_PATH`

```bash
LD_LIBRARY_PATH=[your current LD_LIBRARY_PATH var (if you have set before)]:/app/vendor/pdftk/lib
```

# LICENSE

MIT. See LICENSE for more information.

# Credits

Mostly taken from https://github.com/millie/heroku-buildpack-ruby-pdftk.
Thanks millie for the buildpack and the binary for pdftk:
https://github.com/SirRawlins/pdftk-source

Thank you ddolar for the super rad
https://github.com/ddollar/heroku-buildpack-multi.
