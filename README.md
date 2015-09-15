summit-help
===========

This project contains contextual help for the Summit research administration application.

Files in this project are organized in a hierarchical folder structure that roughly corresponds to the UI structure within the Summit application.

Folder and files names use *camel-case* conventions.
* The first letter of each name is a lower-case letter.
* Every whole word after the first word has an upper-case first letter.

In this structure each help text item (e.g. for a field) is stored in a separate file.  Each file is named for the field (or other UI component) whose help text is stored in the file.  The text in the file can use [Markdown] (https://help.github.com/articles/markdown-basics/)
to express formatting such as emphasis, bulleted lists, etc.

File names containing help text have `.md` as the filename suffix.  This lets the editor and other tooling in the system know that the file contains Markdown text.

The full path to a help text file is used by the Summit build system to associate fields and other UI components with the appropriate help text.  For example, the help file text at `summit/proposals/editor/generalInformation/proposalLabel.md` contains the help text for the **Proposal Label* in the proposal editor.

When writing help text, your editor should be set to wrap automatically at the right margin.  You should use the `Return` key only to separate paragraphs.

Files named `README.md` are ignored by the Summit build system.  You can place them anywhere in the folder structure of this project to provide helpful information for people who write help text (help for help!).
