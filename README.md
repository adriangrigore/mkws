# [`mkws(1)`](https://mkws.sh) 
<p>Efficient Static Site Generator</p>

<pre>
<img src=https://mkws.sh/images/gha.svg width=806 height=96>
</pre>

## Requirements

A UNIX like operating system is recommended like [macOS](https://www.apple.com/macos/), [Linux](https://kernel.org) or [BSD](https://en.wikipedia.org/wiki/List_of_BSD_operating_systems) variant (our favorites are [OpenBSD](https://openbsd.org) and
[Void Linux](https://voidlinux.org/)). Also, familiarity with the command line is good to have. `mkws(1)` can also run on [Windows](https://www.microsoft.com/windows)
via the [Windows Subsystem for Linux](
https://docs.microsoft.com/en-us/windows/wsl/install-win10).

## Installation (applies to [Linux](https://kernel.org))

You'll have to download [https://mkws.sh/mkws@4.0.0.tgz](
https://mkws.sh/mkws@4.0.0.tgz). Once you have the archive, unpack it and rename the newly created directory:

```sh
mkdir -p ~/src/
cd ~/src/
tar -xzfv ~/Downloads/mkws@4.0.0.tgz
mv ws.sh example.com
```

## Make web site

Create an `index.upphtml` file, it will be preprocessed with[`pp(1)`](https://mkws.sh/pp.html), and run `./bin/mkws` with the url of your web site:

```sh
cd example.com
cat <<EOF > index.upphtml
<p>
#!
echo hello, world
#!
</p>
EOF
./bin/mkws https://example.com
```

You can create more `*.upphtml` files to make additional pages, the layout file is held in `./share/l.upphtml`.

Also, you can always modify your `./bin/mkws` script, if it's the case.
