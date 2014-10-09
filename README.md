hackernews [![Hackage](https://img.shields.io/hackage/v/ses-html.svg?style=flat)](https://hackage.haskell.org/package/hackernews)
==========
Hacker News API for Haskell

###Documentation
<https://github.com/HackerNews/API>

###Tests
```bash
cabal configure && cabal test
```

```bash
Hacker News API Tests
  - Retrieves a Story
  - Retrieves a Comment
  - Retrieves a User
  - Retrieves a Poll
  - Retrieves a Pollopt
  - Retrieves Top Stories
  - Retrieves Max Item
  - Retrieves Updates

Finished in 0.0019 seconds
8 examples, 0 failures
```

###Usage
```haskell 
module Main where

import Web.HackerNews (StoryId (..), getStory)

main :: IO ()
main = getStory (StoryId 8863) >>= print
```

```bash
Just (Story {
            storyBy = "dhouston"
          , storyId = 8863
          , storyKids = [8952,9224,8917,8884,8887,8943,8869,8958,9005,9671,8940,9067,8908,9055,8865,8881,8872,8873,8955,10403,8903,8928,9125,8998,8901,8902,8907,8894,8878,8870,8980,8934,8876]
          , storyScore = 111
          , storyTime = 2007-04-04 19:16:40 UTC
          , storyTitle = "My YC app: Dropbox - Throw away your USB drive"
          , storyType = "story"
          , storyUrl = "http://www.getdropbox.com/u/2/screencast.html"
          })
```