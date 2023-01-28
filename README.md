# General Guidance for presentations, papers, and code
Zhonghua Zheng (zhonghua.zheng@outlook.com)

## Table of Contents

- [presentations](#presentations)
- [papers](#papers)
- [code](#code)

## presentations

<details><summary><em>[Click to expand]</em></summary>

- PowerPoint templates: ([link](https://www.staffnet.manchester.ac.uk/brand/visual-identity/guidelines/presentations/))

- Beamer: [overleaf themes](https://www.overleaf.com/edu/theuniversityofmanchester#templates) or [Mark Kambites’ Beamer theme](http://www.maths.manchester.ac.uk/~mkambites/software.php)

  - To make the purple background and white text for [Alex's theme](https://www.overleaf.com/latex/templates/university-of-manchester-presentation-beamer-template/rwcrzjmzcdyn) (from overleaf) based on the [blog](http://amundy.co.uk/2014/01/11/new-introduction-to-beamer-theme.html):

    ```
    \documentclass[11pt,aspectratio=169,ignorenonframetext,t]{beamer}
    AND
    \usetheme[darktitle,dark,framenumber,titleframestart=1]{UoM_alex}
    ```
    
</details>

## papers

<details><summary><em>[Click to expand]</em></summary>

1. name the repo `paper_xxx_journal`, e.g. `paper_UHWs_acp`

2. select `Add .gitignore:TeX`

3. add `*.DS_Store` and `paper_xxx_journal.pdf` (`paper_UHWs_acp.pdf`) to the `.gitignore` via webpage

4. create the following folders for different paper versions  
   - 0_template (this will help you compare different template versions) 
   - 1_draft
   - 2_preprint
   - 2_manuscript
   - 3_reviews_1
     - decision letter (file(s)) 
   - 3_revised_paper_1
     - response_to_reviews (folder)
     - manuscript (folder)
     - submission_suammry (folder or file)
   - 4_reviews_2
     - decision letter (file(s))  
   - 4_revised_paper_2
     - response_to_reviews (folder)
     - manuscript (folder)
     - submission_summary (folder or file)
   - ...
   - final_proofs   
5. within each `manuscript` folder
   - name the latex file the same: `paper_xxx_journal.tex` (e.g. `paper_UHWs_acp.tex`)
   - name the bibtex file `refs_xxx_journal.bib` (e.g. `paper_UHWs_acp.bib`)
   - make a subdir for graphics called `graphics`, which includes all figures (we can reuse the the figures in other folders) 

</details>

## code

<details><summary><em>[Click to expand]</em></summary>

1. name the repo `code_xxx_journal_private`, e.g. `code_UHWs_acp_private`

2. select `Add .gitignore:Python` (or others)

3. add `*.DS_Store` to the `.gitignore` via webpage

4. create the following folders for different paper versions  
   - misc
   - model (optional)
   - data (optional, we must deposit data in a FAIR aligned repository)
   - 0_scratch  
   - 1_draft
   - 2_submitted (you will copy all the code here to the group repository `code_xxx`, e.g. `code_UHWs`)
   - 3_revised_paper_1  
   - 4_revised_paper_2
   - ...
   - final_proof   
   
5. create [symbolic link](https://apple.stackexchange.com/questions/115646/how-can-i-create-a-symbolic-link-in-terminal)
   ```bash
   ln -s ./data ./0_scratch/data
   ln -s ./data ./1_draft/data
   ln -s ./data ./2_submitted/data
   ...
   # to remove the link
   # rm -rf ./0_scratch/data
   # rm -rf ./1_draft/data
   # rm -rf ./2_submitted/data
   ...
   ```
   
6. Before submitting the preprint and manuscript for the first time, using `2_submitted` to check the code

</details>
