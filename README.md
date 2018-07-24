summit-help
===========

This project contains contextual help for the Summit research administration application.

Files in this project are organized in a hierarchical folder structure that roughly corresponds to the UI structure within the Summit application.

Folder and files names use *camel-case* conventions.
* The first letter of each name is a lower-case letter.
* Every whole word after the first word has an upper-case first letter.

In this structure each help text item (e.g. for a field) is stored in a separate file.  Each file is named for the field (or other UI component) whose help text is stored in the file.  The text in the file can use [Markdown](https://help.github.com/articles/markdown-basics/)
to express formatting such as emphasis, bulleted lists, etc.

File names containing help text have `.md` as the filename suffix.  This lets the editor and other tooling in the system know that the file contains Markdown text.

The full path to a help text file is used by the Summit build system to associate fields and other UI components with the appropriate help text.  For example, the help file text at `summit/proposals/editor/generalInformation/proposalLabel.md` contains the help text for the **Proposal Label** in the proposal editor.

When writing help text, your editor should be set to wrap automatically at the right margin.  You should use the `Return` key only to separate paragraphs.

Files named `README.md` are ignored by the Summit build system.  You can place them anywhere in the folder structure of this project to provide helpful information for people who write help text (help for help!).

## Linking Help Content

To prevent the need to have the same help text in multiple locations, you can simply link to another file.

If you wish to link a file, use a `.ln` file extension with contents being a relative path to the intended contents.

Note - If a single field has two files with `.md` and `.ln` extensions, the `.md` will take precedence and be used for display.

### Relative Paths

The contents of the `.ln` file uses a relative path to locate the actual help content.  A relative path is simply the name of the file, relative to the current path's location.  To navigate up a directory, simply use `../`.  The example below provides a demonstration of using a relative path.


### Linking Example

**/summit/proposals/editor/generalInformation/programType.md**
```
A description of the type of work.  If more than one description fits, use the type that best describes the majority of work:

- RESEARCH: Basic or applied research and development activities; conferences for the development or exchange of research information; development of new educational methods; evaluation of State and Federal Programs
- INSTRUCTION: On-campus or off-campus instruction for credit; scholarships and fellowships; student services; instructional equipment; improvement of instructional programs
...
```

**/summit/proposals/initiator/details/programType.ln**
```
../../editor/generalInformation/programType.md
```
- In order to get the `generalInformation` folder from the `details` folder, we have to navigate up two directories (`../../`).

- Action Help lives in the checklist folder.  Append a "-action-help" to the filename.  for example, a checklist item who's filename would be "classifiedResearch.md" would have an action help filename of "classifiedResearch-action-help.md"

