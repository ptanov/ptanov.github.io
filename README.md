For more information see [about.md](about.md).

- This blog is available on <https://blog.plamen.name/>.
- To locally run this blog (while editing) run:
 - `docker run --rm -p 4000:4000 -v "$(pwd):/srv/jekyll" -it jekyll/jekyll jekyll serve --watch`
 - then go to <http://localhost:4000/>
- To add tags (before committing) run:
 - `docker run --rm -v "$(pwd):/site" -w /site python /bin/bash -c 'curl https://raw.githubusercontent.com/qian256/qian256.github.io/master/tag_generator.py -o /tmp/tag_generator.py && python /tmp/tag_generator.py'`
