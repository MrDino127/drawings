# drawings

The drawings on my site, [nico.kodeko.org](https://nico.kodeko.org). The site shows whatever is in here: add, change or
delete a drawing, push, and a couple of minutes later the site has it.

## Folders

Each folder is a category, and its name is the filter button on the site. A new folder (say `comms`) is a new category.
An empty folder doesn't show up.

Pictures can be .png, .jpg, .webp, .gif or .avif. Other files (.kra, .svg, .ico...) can sit in the folders too; the site
skips them.

To keep something off the site, start its name or its folder's name with `_`, like `_old stuff`. Anything with
"DO NOT REPOST" in its name is skipped too.

## Info about a drawing

Next to a drawing you can put a text file with the same name, ending in `.txt`:

    fan art/Ralsei.gif
    fan art/Ralsei.txt

Inside, one thing per line:

    title: Ralsei
    alt: Ralsei from Deltarune in pixel art, in his green hat and pink scarf
    featured: yes
    hidden: yes

- **title**: the name shown on the site. Without it, the file name is used.
- **alt**: what the picture shows, in words, for people who can't see it (blind people use these). Without it, the
  title is used.
- **featured: yes** shows it bigger.
- **hidden: yes** keeps it off the site, but here.

All of it is optional, the .txt file too. Leave out the lines you don't need. A line starting with `#` is a note to
yourself and gets ignored. If you rename a drawing, rename its .txt as well.

## Order

Newest first: a drawing you add shows up at the front. Moving it to another folder or renaming it doesn't change its
place. Drawings added at the same time go in alphabetical order.

## The rebuild

`.github/workflows/rebuild-site.yml` is what tells the site to rebuild after each push. Leave it in. It needs a secret
called `SITE_DEPLOY_HOOK` (Settings → Secrets and variables → Actions); if it's missing, the Actions tab says so.
