# Sec-Notes

موقع مقالات شخصي مبني بـ [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

## تشغيل محلي

```bash
python -m venv .venv
source .venv/bin/activate        # على ويندوز: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

افتح http://127.0.0.1:8000

## النشر على GitHub Pages

1. اعمل ريبو جديد على GitHub وارفع الملفات دي:

```bash
git init
git add .
git commit -m "init"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

2. الـ workflow هيشتغل لوحده وينشئ فرع `gh-pages`.
3. روح **Settings → Pages** واختار Branch = `gh-pages` / `root`.
4. الموقع: `https://USERNAME.github.io/REPO/`

## النشر على GitLab Pages

امسح مجلد `.github/` وسيب `.gitlab-ci.yml`، وارفع على GitLab. الموقع هيطلع على
`https://USERNAME.gitlab.io/REPO/`.

## دومين خاص

1. أنشئ ملف `docs/CNAME` جواه سطر واحد: `blog.yourdomain.com`
2. عند مزوّد الدومين اعمل CNAME record يشاور على `USERNAME.github.io`
3. Settings → Pages → اكتب الدومين وفعّل Enforce HTTPS

## إضافة مقال جديد

1. أنشئ ملف في `docs/articles/my-article.md`
2. أضف سطره في `nav` داخل `mkdocs.yml`
3. أضف كارت في `docs/articles/index.md`
4. `git push` — وخلاص

## قبل ما ترفع

بدّل `username` و `Your Name` و `you@example.com` في `mkdocs.yml` و `docs/index.md`.
