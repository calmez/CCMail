# CCMail
A concept mail client created in [Squeak](http://squeak.org) with [Vivide](https://github.com/hpi-swa/vivide)

To install the Vivide tool scripts displaying the mail data do:

```smalltalk
ViScriptArchive mergeAll.
```

To create a new archive backed by a Maildir do:

```smalltalk
| myArchive |
myArchive := MailArchive archiveWithDataSource: MailArchiveDataSourceMaildir new.
```

To read the archive from disk do:

```smalltalk
myArchive synchronize.
```

:warning: Currently the Maildir will be expected to be in the same folder as your image under the name ```Maildir```. This directory then can contain the Maildir boxes that should be read in.

:warning: Nested Maildir boxes will currently not be read in.
