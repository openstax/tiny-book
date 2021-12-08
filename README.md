This is a commit on a branch so we can test branch and commit builds. The tests do not depend on the actualy contents of this change. so keeping this branch up-to-date should be painless.

This repo contains a small book.
Here are the relevant files and directories:

- [canonical.json](./canonical.json)
- [collections/](./collections/)
- [media/](./media/)
- [modules/](./modules/)


# Questions

- why does /media/ have to exist even if there are no images?
- why do module CNXML files need a metadata element?
- why do we still need the `version-at-this-collection-version` attribute? (cnx-epub requires it during assembly)
- we still require collxml module entries to have a title
- It seems the slug entry in the collxml must match the name of the file (`slug1.collection.xml`). Is that necessary? (`git-link` step fails)
- The validation error for a missing license is not very helpful. jsonschema just says `None: None is not of type 'string'`
- why is the module & collection UUID an element instaed of an attribute on the root element?
- why does the module still need a content-id? (this seems to be the case since I'm trying to figure out why the module uuid is disappearing during assembly)
- Are the `.vscode/settings.json` and `.gitignore` (for XSD) really necessary?
