# Building Boo code editor #1

![Boo sticker](https://raphamorim.io/assets/images/posts/boo-sticker.png)

I decided to document Boo code editor development for good (or bad).

Suppose you have any interest in it. Please stick with me in this article.

### Brief Story

In 2024 I have started a proof of concept of Boo, which back in time was called Yoyo. The proof of concept didn’t have [tree sitter](https://tree-sitter.github.io/tree-sitter/), language server protocol, or anything fancy. It was built with JavaScript (and it was using a lot of memory). It was solely made to test navigation and edition between files.

The prototype development was quick to finish. JavaScript and the Web are part of excellent tools to build prototypes. You do not need to care about rendering stuff, shaders, IMEs, native API, etcetera; it just works out of the box. The side effect though, is that in performance terms isn't the best.

I wanted to prove to myself: ok, Boo editing system wasn't crazy and could work for anyone that has zero experience with programming. After a few iterations, the idea I took from my notebook drafts was working fairly well: no mouse dependency whatsoever, you don’t need it anymore. No necessity to feel like playing guitar while editing a file.

Me debugging Boo while frustrated with the performance so far whenever pressing enter lol.

<video autoplay loop playsinline muted style="width: 100%">
  <source src="https://raphamorim.io/assets/videos/boo-quick-demo.webm" type="video/webm" />
</video>

Btw that (^) was fixed already.

### A new navigation system

Boo is created over a new navigation system called Zaap, which is an attempt to make editing easier for mouse-free users while keeping it intuitive for non-programmers. The navigation system is built to run everywhere else besides Boo (through C bindings, like tree sitter), so if you don't like Boo you can port it to your favorite editor.

Zaap has been tested with a few non-programmers and worked fairly well, although every user had a learning curve of averaging 2 to 4 days to get used (this is something that I feel needs improvement).

Would Boo support VIM, Emacs keybindings? Man, I have been asked a lot about it in the past months and would like to highlight it isn't in my plans. While I look to VIM and Emacs as my references for great editors, I am trying to create something that feels different and that could give me the freedom to be innovative and explore other ideas. If I commit to support x or y, then every single idea I have will need to be aligned with the commitment.

### Hybrid editor

The editor works already as a graphical user interface (GUI) or terminal user interface (TUI). It is up to you to decide where you want to work. Boo has an integration system that I will talk more about in the future, that allows you to use both in a way that is helpful.

### AI where matters

Boo already works with Github Copilot and allows you to integrate to your favorite AI tool (well, this second part still needs a bit of love ha!). However, the biggest goal is to make AI completely optional, disabled by default, without affecting users that doesn't care about it.

The biggest problem regarding editors with AI nowadays is that can feel or give the perception of being bloated. I assume no one wants that, right?

### When it will be released?

No idea!

This year has been quite busy for me as a new parent and in a [new job](/joining-charm). The few time that I had was to work on [Rio terminal](https://github.com/raphamorim/rio), however I am in no rust, I want to build something fun and it sure will take time.

I hope that you found this chat interesting. Given it's our second time talking, there were so many more things I could’ve covered, but I’ll save them for the future.

-

If you want to keep up to date, follow me on [Twitter](https://x.com/raphamorims), [Bsky](https://bsky.app/profile/mustache.bsky.social) or [Mastodon](https://mas.to/@mustache).
