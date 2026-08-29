git clone https://github.com/rashidul-cs/rashidul-cs.git && \
cd rashidul-cs && \
curl -fL "https://gh.crafter.run/rashidul-cs?theme=dark&cols=140" -o dark_mode.svg && \
curl -fL "https://gh.crafter.run/rashidul-cs?theme=light&cols=140" -o light_mode.svg && \
printf '<picture>\n  <source media="(prefers-color-scheme: dark)" srcset="dark_mode.svg" />\n  <source media="(prefers-color-scheme: light)" srcset="light_mode.svg" />\n  <img alt="rashidul-cs'\''s GitHub profile" src="dark_mode.svg" />\n</picture>\n\n' | cat - README.md > temp_readme.md && mv temp_readme.md README.md && \
git add dark_mode.svg light_mode.svg README.md && \
git commit -m "feat: add gh-ascii profile card" && \
git push origin main
