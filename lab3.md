# Lab Report 3

This tutorial explains 4 command-line options for the command `less`. We use `less` to view a portion of a file from the command-line without printing the entire text, hence the name LESS.

All of the following options were found using the Wikipedia page for [less](https://en.wikipedia.org/wiki/Less_(Unix)).


## Option 1: -N

This option displays line numbers next to the text! This is especially helpful when viewing code.

```
[cs15lwi23acc@ieng6-201]:berlitz2:288$ less -N California-History.txt

1
2
3
4
5 A Brief History
6 The first wave of California immigrants arrived somewhere between 20,000 and 35,000 years ago<C2><A0><E2><80><94><C2><A0>wandering Asiatic tribes who entered the America      
6 n continent via the Bering Strait, which at that time was dry land, or perhaps covered in ice. In the succeeding centuries, their descendants continued to push south and      
6  east, and eventually spread out to people the whole of the continent from Alaska to Patagonia. The tribes who decided to settle in what is now California were fortunate      
6  in their choice of homeland. The climate was very pleasant, and food was sufficiently plentiful for them to avoid the constant warfare that plagued many tribes elsewher      
6 e in the Americas.
```

As shown, the option displays the numbers of the lines alongside the text of the document. The repeating numbers signify a line longer than is able to be displayed. Let's see it on a different file.

```
[cs15lwi23acc@ieng6-201]:berlitz2:288$ less -N Barcelona-WhatToDo.txt

1
2
3
4
5 What to Do
6 Shopping
7 Barcelona is at least Madrid<E2><80><99>s equal as a shopping capital. As a city of eminent style and taste, Barcelona abounds in fashion boutiques, antiques shops, and       
7 art galleries. Design is taken very seriously here.
8 Shopping is also extremely pleasant in Barcelona, as the city hasn<E2><80><99>t yet been overtaken by large look-alike malls and homogenous American or Euro stores. Cata      
8 lonia still thrives on family-owned shops, and window shopping along the Rambla de Catalunya or Passeig de Gr<C3><A0>cia is a delight. Remember that with the exception o      
8 f the big department stores, most shops are closed between 1:30 or 2pm and 4 or 5pm, and stay open until 8pm or later. Many smaller stores also close Saturday afternoons      
8  and Sundays.
```

These are just the first few lines of the document. The output is very similar to the above example, but with new text for the different document. Overall, this option is helpful for viewing longer documents, such as code where tracking edits and additions requires attention to detail. It is also generally helpful to keep your place while viewing the file.


## Option 2: -S

This option disables text-wrapping, forcing the user to scroll. This could be useful when formatting is important or when viewing directory paths/other long strings.

```
[cs15lwi23acc@ieng6-201]:berlitz2:291$ less -S China-History.txt

A Brief History
Hundreds of thousands of years before China was to become the world<E2><80><99>s longest-running civilization, the prologue was enacted by means of the flicker of a carefully te
Technologically and sociologically, it was a phenomenal breakthrough: with fire, communities could live year <E2><80><99>round in one cave, in which cooking and even smelting co
The First Dynasty
The confluence of mythology and history in China took place around 4,000 years ago during what is referred to as the Xia (Hsia) Dynasty. This was still the Stone Age, but the pe
During the second of the quasi-legendary dynasties, the Shang (from about the 16th to 11th centuries b.c.), the Chinese developed an interest in art. Careful geometric designs a
```

When copy and pasted directly from the output, the text looks incomplete as shown above. However, this is just because the text displayed requires side-scrolling in order to view fully.

Let's try combining the two options we just learned!

```
[cs15lwi23acc@ieng6-201]:Abernathy:304$ less -N -S ch3.txt

1
2
3
4
5 In 1911, John Wanamaker opened his flagship store in downtown Philadelphia. The twelve-story building, with its forty-five acres of floor space, was the largest of its time devoted
6 Wanamaker had been in the forefront of retailing for more than thirty years by the time he opened this store. His goal was to provide the elegant shopping experience of major Europ
7 Sixty years after the opening of Wanamaker<E2><80><99>s Philadelphia store, another entrepreneur synthesized a set of existing technologies and, along with a number of other retail
8 As we have emphasized, the current retail revolution<E2><80><94>involving new information technologies, new product labeling, and new methods of distribution<E2><80><94>has driven 
9 This chapter will examine the differences between the traditional re-tail model and lean retailing. We explore how the set of practices that traditional retailers drew on to mercha
```

As expected, the text does not wrap, and is also accompanied by line numbers. This option is helpful for documents where visual formatting is important, like written text or classpaths. However, this option would likely make it more difficult to screenshot or copy the output, because as seen above, the terminal cuts off text at the edge of the screen.


## Option 3: -X

This option leaves the text on the screen, similar to `cat`.

```
[cs15lwi23acc@ieng6-201]:Abernathy:305$ less -X ch15.txt 

More than a century ago a major wave of innovations in distribution and production led to the modern department store, the mail-order house, and the chain store, and reshaped their suppliers. The present transformation of retail and manufacturing engendered by new information technologies, production methods, and management practices also fundamentally alters the manner in which industries and firms take raw materials, turn them into a profusion of products, and deliver them to consumers. Although these developments are very much a work in progress, information-integrated channels of production and distribution are emerging.
Such channels are not unique to retail-apparel-textile relations but have arisen in a wide variety of consumer product industries in which retailing practices are undergoing similar changes. The developments reported here offer a prototype of the new links among manufacturers, other suppliers, retailers, and consumers.
In fact, the transformation has been gradual and is still under way. Only as recently as the mid-1990s has integration risen to critical levels, providing a clear picture of what channel relations will look like in the future. Information integration has reshaped much of the retail-apparel-textile channel, yet further transformation is likely in the decade ahead, not only for these linked industries, but for consumer product sectors in gener
```

Hold on, this option looks exactly like a regular call to `less`! That's because it is! The text is displayed like usual, but the difference is that it remains even after exiting with `q`. 

Just for fun, let's combine all three so far.

```
[cs15lwi23acc@ieng6-201]:Abernathy:307$ less -S -N -X ch6.txt 
 
1
2
3
4
5 William Dillard<E2><80><99>s simple maxim1 succinctly captures the central<E2><80><94>and perennial<E2><80><94>inventory challenge facing retail managers. To make a sale, a retaile
6 The main goal of retail inventory strategy is to maximize profitability by managing the inherent tension between stocking too much and stocking too little. Retail buyers of old gra
7 Conceptually, retail inventory management is straightforward enough: Forecast demand for a product; order the product in the appropriate quantity; stock it in the right retail loca
8 The forecasting and inventory models presented in this chapter are not new; they have been recommended for years by statisticians and operations researchers.3 However, until the 19
9 The Retail Forecasting Challenge
10 We first turn to the problem of forecasting sales in retail stores. Imagine trying to predict how many women will walk into a particular downtown Boston store next week prepared to  
```

The output looks exactly like our previous command using just `-S -N`, but this one will remain in the terminal. 

Overall, the significant difference between `-X` and `cat file.txt` is that this option adheres to the regular rules of `less` by only displaying one screen's worth of information at a time. The text that remains is ONLY that which was shown with the command, NOT the entire document. This option is helpful for when you only need to access the beginning or a specific section of a particularly long file.


## Option 4: -F

I found this one indirectly through the Wikipedia link, as I found the `-?` help option there and used it to find this one. This option will quit the `less` display if the text is shorter than a screen length.

```
[cs15lwi23acc@ieng6-201]:Abernathy:310$ less -F ch1.txt

In the late 1940s, Bond Stores, the largest men<E2><80><99>s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.
Fifty years later, it is hard to imagine a retailer<E2><80><94>be it a high-end department store, mass merchandiser, or catalog service<E2><80><94>limiting an individual customer<E2><80>  
<99>s clothing purchase. Retailers collect detailed point-of-sales information that reflects the real-time demand for goods by consumers. Through new computer systems, they share this information with suppliers who, in turn, can ship orders within days to automated distribution centers. The contemporary equivalent of Bond Stores now has a much better chance of avoiding stock-outs of popular items and the inventory gluts that lead to costly markdowns. By the same token, the overall risk associated with fickle consumers, numerous selling seasons, and segmented markets<E2><80><94>along with fierce overseas competition<E2><80><94>has currently made this a tough arena for American retailers and manufacturers.
```

Attempting to use this option on a regular-length file will just behave normally. Now let's create a short text file and attempt the option again.

```
[cs15lwi23acc@ieng6-201]:Abernathy:310$ echo "Hello there" > generalKenobi.txt
[cs15lwi23acc@ieng6-201]:Abernathy:311$ less -F generalKenobi.txt
Hello there
```

Instead of showing the usual screen-length display, the message was printed to the terminal and `less` was immediately quit. With shorter text files such as the above, this option seems to be functionally similar to `cat`. `less -F` is helpful because it instantly tells you whether or not a file's content is short enough to fit on one screen length, whereas using `cat` without knowing the file's contents might accidentally lead to a huge log of text.

