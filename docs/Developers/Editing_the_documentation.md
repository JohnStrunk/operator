# Editing the documentation

The documentation resides in the main Anthill repo, under the `/docs`
directory as a set of markdown files.

Documentation is checked as a part of the Travis CI infrastructure, but it is
actually build directly by ReadTheDocs, triggered by a webhook upon commit.

If you are making changes to the documentation or its configuration, you
probably want to edit and view your changes locally. This can be done
relatively easily using `mkdocs`.

## Building locally

The mkdocs tool can be installed via pip:

```sh
pip install mkdocs
```

You can then view live updates as you make documentation changes by starting
the documentation server.

From the top directory of this repo:

```sh
mkdocs serve
```

By default, this will start a web server on your local machine, allowing you to
view the documentation by pointing your browser at:
[https://localhost:8000](https://localhost:8000)

## Documentation hints

The placement of the markdown files and how they are named affect the layout of
the documentation site. Some things to keep in mind:

- The menu bar across the top has an entry for each markdown file in the top
  `/docs` directory. It also has a drop-down for each directory that contains
  markdown files.
- Menus (top and dropdown) are sorted alphabetically by the name of the file.
- File names become the entries in the menus. Case is preserved, and
  underscores become spaces.
- Each page has its outline displayed on the left.
- Links within the documentation should be relative links to the `*.md` source
  file. The documentation builder will make it point to the correct place.

For more information, check out the documentation at
[MkDocs](https://www.mkdocs.org/).