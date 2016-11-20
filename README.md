A 46th fork of [Hacker theme](https://github.com/CodeDaraW/Hacker) for [Hexo](https://hexo.io/)


## What's new

- Added 'Read more' link to articles in Index page. Horray! Usage: add `<!-- more -->` to a post to cut it.


## Installation

Clone into `themes` folder:

```bash
$ git clone https://github.com/ciases/Hacker themes/Hacker
```

Then apply the theme in hexo global configuration file `_config.yml`:

```yaml
theme: Hacker
```

Now all is in order, just enjoy~

__Notice: After every update, you'd better run command `hexo clean` to clean cache files before Hexo generating, in case of some problems cache files bring.__


## Configure
In the theme configuration file `_config.yml`:

```yaml
# duoshuo comment
duoshuo: true
duoshuo_name:

# disqus comment
disqus: false
disqus_shortname:

# google analytics
googleTrackId:
```


`duoshuo`: `boolean`, use duoshuo or not;
`duoshuo_name`: `string`, your duoshup ID, please don't use other people's IDs。

`disqus`: `boolean`, use disqus or not;
`disqus_shortname`: your disqus site shortname.

`googleTrackId`: your Google Analytics ID, Hacker will not use Google Analytics if it's empty.


## TODO
- add screenshots


## License
GPL(General Public License)
