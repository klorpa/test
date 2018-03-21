# Contributing To This Repository

## Overview
The following information outlines the guidelines set by this repository's maintainer. We previously did not have any major contributor guidelines, and while this led to a fairly relaxed and unstructured work environment, it also led to absolute chaos when repository maintainers disappeared and other people had to sort through the mess they left behind. These guidelines aim to create a predictable and uniform workflow. These guidelines may be updated at any time.  

Note that each repository may have different guidelines; please contact the maintainer listed in this repository's README for more information.

## Guidelines
If you have been given Developer access, please create a new branch in the Contributors group (eg; `contributors/[contributor name]`, replacing `[contributor name]` with your Discord or GitGud name).  

Please do not push anything to other contributors' branches unless you have been given permission to.

Do not create more than one branch. If you feel that you need additional branches, please contact the repository maintainer first.

Please keep a Translation file (one should be supplied in the `#Translation` directory) up to date with the files you have translated, whether they are complete or in-progress, and whether you have added any custom code to said files. Additionally, in this file, please list whether your branch can be merged into the master branch freely, or at your discretion only.

Contributors are responsible for ensuring that their branch is up to date with the master branch. If your branch requires significant work to merge due to being out of date, it will not be merged until it is corrected.

Contributors are responsible for checking the repository's commit history regularly to familiarize themselves with what other contributors are working on, and to avoid a duplication of work. In the event that one file is translated by two different people, the most accurate translation will be chosen when merging.

Do not comment out (eg; 'hard disable') events or dialog. If you don't feel like translating them, just move on and let someone else do it. If you don't like the content of said event, we can discuss adding a toggleable event filter if others agree. Unless it is to prevent a bug that must be fixed on the Japanese end, no events or dialog should be commented out.

Please add comments to any code modifications you make to aid merging updates from the Japanese branch. Additionally, please list lines that contain custom code in the Translation file. The Translation file likely has existing lines and associated comments that you can use for reference. You do not need to add comments to code that is purely for aesthetic purposes (eg; string formatting). Just be sure to mention in the Translation file that custom formatting was used.

Please use a separate file for English/Custom functions if possible. All custom functions should go in the `ERB/Translation` directory.

When translating dialog, please try to keep the overall character in mind. The translation may not be 100% correct, but the tone/personality/etc of the character should be consistent.

General sentences use normal capitalization/punctuation. Menu items and actions use Title Case without punctuation.

When shortening a word, please add a comment with the unshortened word for reference if the shortened word's meaning might not be immediately apparent.

If you translate a word, but are uncertain of its accuracy, please add a comment saying so. It may be re-checked by someone else.

Please don't half-ass the translations.

Please add any bugs you encounter to the repository's Issues page, and list whether they are specific to your branch or are also encountered in the master branch.

## Online Translation Resources

[Google Translate](https://translate.google.com/#ja/en/)  
[Microsoft Neural Machine Translation](https://translator.microsoft.com/neural)  
[Linguee](http://www.linguee.com/japanese-english)  
[Jisho](http://jisho.org/)  

See also: The eragames' modified version of Chii Trans Lite.

## Note The Following
Developers will not be able to push to the game/master or game/japanese branches.  
Consistently active developers may be chosen as additional repository maintainers.