# Stretch Goals for the *nix Scavenger Hunt

The following goals are meant to provide a way for more experienced users to
extend their knowledge of the *nix command line.

* Use `curl` to look up the URL `http://www.imdb.com/title/tt0070948/`. The title of this film will lead you to the answer. *What is the answer?*

I ran:
``` 
$ curl http://www.imdb.com/title/tt0070948/ | grep --color -i "title"
```
Found the movie title, then:

```
dineen@laptop:/mnt/c/Users/dinee/Desktop/wats1030-intro-to-unix$ grep -r Zardoz
challenge_files/test2/explicabo_dolor.txt:Aperiam ipsam perferendis ut non est. Harum numquam officia veniam ea vel dolor. Unde vel vitae minima optio quas aliquam vel. Enim voluptatem autem culpa saepe. Alias ipsa Zardoz praesentium occaecati qui quaerat voluptas.
```

I'm guessing the answer is the folder:  challenge_files/test2/explicabo_dolor.txt
