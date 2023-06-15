# Thai Script on LaTeX

## Description
This script enables the usage of Thai script in a LaTeX document
while little to none modifications are needed in the source code.

## Author
Prachya Boonkwan (NECTEC, Thailand) <br>
kaamanita at google mail dot com

## Usage

1. Create a new folder called `fonts`.
2. Upload the font of your choice to this folder. In most cases, you may want to consider Sarabun on Google Font Collection (https://fonts.google.com/specimen/Sarabun?query=sarabun).
3. In your source code, place these lines in the preamble.
   
       \usepackage{thaiscript}
       \usethaifont{Sarabun}

   Note that the font name `Sarabun` can be replaced by the font of your choice.
4. Compile your source code with XeLaTeX. On Overleaf, please configure your compiler by:
      1. Click `Menu`
      2. Go to `Settings` > `Compiler`.
      3. Change it to `XeLaTeX`.
6. You can type in English and Thai texts without having to use any specific command for a Thai text. The script will detect Thai texts and switch to the Thai font automatically.
7. That's it. You can now use Thai script on your LaTeX document.

## Cautions

1. Once you enable Thai script, the base line (size of text lines) will be automatically stretched by 1.3 times to accommodate Thai vowels and tone marks. If you don't want this feature, please add this line right after the above two lines.
       
           \renewcommand\baselinestretch{1}
       
   This command will take the baseline back to normal.
2. Until now (June 2023), arXiv doesn't allow any submissions to be compiled by XeLaTeX, disabling the use of this script as a result. The current workaround is to write the content in English as much as possible and to introduce Thai examples as figures and illustrations instead. Apologies for any inconveniences this may cause.
