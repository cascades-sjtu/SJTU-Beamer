# SJTUBeamer 🤓

Welcome! 🥳

This is the beamer template exclusively for Shanghai Jiaotong University students to give a speech on group meeting or course project.

## Usage 🧰

For Overleaf users, you can directly download the zip file from github and upload it to https://latex.sjtu.edu.cn to use this template.

If you want to use this template locally, simply download zip file and run `latexmk -xelatex`.

## Design Philosophy 💭

To design the template as simple as possible, since everyone can modify it according to their preferences with a little knowledge of LaTeX syntax and beamer.

## Contribution 👷

Feel free to file an issue with GitHub Issues. At the same time, PRs are always welcomed.

> After modifying the corresponding source code in src/source, run .github/ci/build_package.sh in bash to build the package and update the sty files.
> For Windows users, before the next edition of l3build is released, please run
```cmd
cd src/source
latex beamerthemesjtubeamer.ins
```
and copy the corresponding files to the correct directory.

## Test Version

You could get different styles from the following keywords.
```latex
\usetheme[maxplus]{sjtubeamer}
% use maxplus/max/min to change covers.
% use red/blue to change main color.
% use light/dark to change dominate color.
% use the following keywords to make different sidebars:
%   miniframes infolines  sidebar*
%   default    smoothbars split	 
%   shadow     tree       smoothtree
% *siderbar is recommended to be used with max option.
```

## Appearance 🧐

**Blue theme cover page**

![page001](https://user-images.githubusercontent.com/4198311/119085675-be619a80-ba36-11eb-878f-609b2882dc35.png)

**Red theme cover page**

![page001](https://user-images.githubusercontent.com/4198311/119085697-c7526c00-ba36-11eb-8a70-296f8f36c2d6.png)

**Normal cover page**

![page001](https://user-images.githubusercontent.com/4198311/118810621-aa0a8a00-b8de-11eb-907e-6342c156ea53.png)

**Red theme slides**

![page004](https://user-images.githubusercontent.com/4198311/118810609-a70f9980-b8de-11eb-84b3-68918c905817.png)
