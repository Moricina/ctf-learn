

## How to build？

CTF Wiki uses [mkdocs](https://github.com/mkdocs/mkdocs) to show its contents. And it is deployed at [https://ctf-wiki.org](https://ctf-wiki.org).

It can also be deployed locally, with the following steps:

```shell
# 1. clone
git clone https://github.com/ctf-wiki/ctf-wiki.git
# 2. requirements
pip install -r requirements.txt
# generate static file in site/
python3 scripts/docs.py build-all
# deploy at http://127.0.0.1:8008
python3 scripts/docs.py serve
```

**A local instance of mkdocs is dynamically updated, for instance when a markdown file is modified, the corresponding page will be modified too.**

If you just want to view it statically, try Docker!

```
docker run -d --name=ctf-wiki -p 4100:80 ctfwiki/ctf-wiki
```
And then access [http://localhost:4100/](http://localhost:4100/) .

