# PepLink Pages

Static GitHub Pages landing page for PepLink.

## Deploy with GitHub Pages

1. Push this folder to the repository that should host the site.
2. In GitHub, open `Settings` → `Pages`.
3. Set `Build and deployment` to `Deploy from a branch`.
4. Select the publishing branch and the `/ (root)` folder, then save.
5. The current site URL is set to `https://tianangleng.github.io/peptide_to_smiles/`.
6. If you add a custom domain, update the canonical URL, sitemap URL, and social image URLs to match that domain.

## Included Files

- `index.html`: full landing page markup and SEO metadata
- `styles.css`: layout and visual system
- `robots.txt`: crawler rules plus sitemap location
- `sitemap.xml`: single-page sitemap
- `.nojekyll`: ensures GitHub Pages serves the repo as a plain static site
- `assets/hero-figure.svg`: hero illustration
- `assets/og-preview.svg`: social preview image
- `assets/favicon.svg`: SVG favicon

## Suggested Repository Metadata

Repository description:

`Peptide ↔ SMILES/SELFIES conversion for monomer peptides with non-canonical residues, terminal modifications, and selected cyclizations.`

Social preview description:

`PepLink converts peptide sequences to SMILES or SELFIES and helps interpret peptide-like SMILES for practical peptide informatics workflows.`

Alternate homepage title:

`Peptide to SMILES and SMILES to Peptide with PepLink`

Recommended GitHub topics:

- `peptide`
- `smiles`
- `selfies`
- `peptide-to-smiles`
- `smiles-to-peptide`
- `cyclic-peptide`
- `noncanonical-amino-acids`
- `cheminformatics`
- `computational-biology`
- `rdkit`

## 同步发布到新旧地址

在本机 `Published_packages/PepLink_Page` 目录提交后，运行 `git push origin main`。
本地 origin 配置了两个 push URL，依次更新 `TianangLeng/peptide_to_smiles` 和 `DragonDescentZerotsu/peptide_to_smiles`。确认两次推送都成功；任何一边失败时解决错误并重试，不要强制推送。

两个仓库均保留 Pages（main，根目录）。旧网站入口会跳转至新站，保留查询参数和锚点；资源文件仍可从旧地址读取。GitHub 网页编辑及其他未配置的克隆不会自动双向同步。

新克隆可在确认 origin 指向新仓库后恢复双推送：

```sh
git config --local --replace-all remote.origin.pushurl https://github.com/TianangLeng/peptide_to_smiles.git
git config --local --add remote.origin.pushurl https://github.com/DragonDescentZerotsu/peptide_to_smiles.git
git remote get-url --push --all origin
```

站点根目录的 robots.txt 由主页仓库维护；本目录的 robots.txt 仅作为项目发布信息。主页的 sitemap.xml 也列出 PepLink 新网址。
