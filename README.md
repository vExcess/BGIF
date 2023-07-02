# BGIF
Better Graphics Interchange Format - It's GIF but better

## History
Khan Academy has a very sandboxed editor that doesn't allow you to display images. However for as long as it has existed people have wanted to display images on Khan Academy. In 2014 Bob Lyon released his revolutionary Imagenator which converts images to strings that can then be displayed on Khan Academy using a simple decoder. However his Imagenator used an ad-hoc encoding which's compression capabilities were not the best. Getting the most compressed image possible is necessary on Khan Academy which restricts you to 750 KB. In 2019 Bob Lyon delivered again having ported a PNG decoder library to KA's environment. PNG compression is quite good, however the decoder itself is 29 KB and not very reliable. In 2021 I ported a JPEG decoder to Khan Academy. JPEG provides extremely good compression however the codec for it is 41 KB. In 2022 I ported QOI to Khan Academy. QOI compression is almost as good as PNG, nearly 50 times faster, and its codec is only 13 KB. I also tried making a GIF decoder, but that failed miserably.

However during all these years my obsession with compression was growing as I experimented with every single compression algorithm my feeble brain could come up with. I attempted to have the best image algorithm yet providing even smaller memory than PNG. Over the years I have released over a dozen different iterations of my own image formats which have grown better over time. I created my own Imagenator which provided far superior compression to Bob Lyons imagenator and only weighed in at a mere 1.6 KB. My last was a format that resulted in images only 1.4x larger than PNG and the decoder was only a mere 1.5 KB. However I have realized that once someone ports a WEBP decoder to KA it's all over. Webp has far superior compression compared to either PNG or JPEG which isn't surprising given that Google has poured a decent amount of money into it. In addition I left KA's limited editor do real programming. As a result for my final image compression endeavor I have decided to ditch the idea of beating PNG and JPEG and turn my focus to beating GIF. The GIF format is unmistakable for its prized charismatic 256 color animated displays. However GIF has flaws making it more complex, bloated, and limited than it should be. I shall create an image format designed for 256 color animated images, however mine will be more customizable in addition to having better compression.
