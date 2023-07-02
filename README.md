# BGIF
Better Graphics Interchange Format - It's GIF but better

## History
Khan Academy has a very sandboxed editor that doesn't allow you to display images the normal way. However for as long as it has existed people have wanted to display images on Khan Academy. In 2014 Bob Lyon released his revolutionary Imagenator which converts images to strings that can then be displayed on Khan Academy using a simple decoder. However his Imagenator used an ad-hoc encoding which's compression capabilities were not the best. In 2019 Bob Lyon delivered again having ported a PNG decoder library to KA's environment. In 2021 I ported a JPEG decoder to Khan Academy. JPEG provides extremely good compression however the codec for it is 41 KB. In 2022 I ported QOI to Khan Academy. QOI compression is almost as good as PNG, nearly 50 times faster, and its codec is only 13 KB. I also tried making a GIF decoder, but that failed miserably.

However during all these years my obsession with compression was growing as I experimented with every single compression algorithm my feeble brain could come up with. I attempted to have the best image algorithm yet providing even smaller memory than PNG. Over the years I have released over a dozen different iterations of my own image formats which have grown better over time. I created my own Imagenator which provided far superior compression to Bob Lyons imagenator and only weighed in at a mere 1.6 KB. My last was a format that resulted in images only 1.4x larger than PNG and the decoder was only a mere 1.5 KB. However I realized that I will never be able to create a better format than Google has already done with WEBP. Therefore rather than me creating another general purpose image format (like PNG, JPEG, WEBP) I decided to create a specialized image format.

## Format Type
PNG already rules the world of lossless image compression and there is no point in trying to beat it. JPEG already rules the world of lossy image compression and there is not point in trying to beat it. WEBP already the best format for the web and there is no way I could beat that either. QOI already is the goto image format for relatively fast compression times. SVG could be improved, but I'm doing bitmap images here not vector graphics. TIFF already is the image format that allows reversable edits. So if I can't win the lossless general purpose category, the lossy general purpose category, the web category, the speed category, the photo editing(?) category, and don't want to get into the vector graphic category what is left? And the only thing that is left is the nostalgic animated meme category which is currently dominated by the GIF format. However unlike the other formats which are pretty much the best they can be for their purpose, the GIF format is really not that great. So if GIF format is so bad then why does everyone use it? The answer is that there has never been a new image format created to be like GIF but better. PNG has an animated feature, but it relies on third party software and PNG wasn't meant to be animated causing animated PNGs to use more memory than a GIF. WEBP images can be animated, but again that wasn't WEBP's original goal. It's goal was to provide better image compression for web images. Therefore unlike other new image formats which were meant to be general purpose, I'm creating one specifically meant to be like GIF but better.

## About
GIF only allows 256 colors. Likewise BGIF also only allows 256 colors. I could very easily make the format capable of storing millions of colors without any significant overhead, but at that point I would just be creating a new general purpose image format. I am artificially restricting the format to 256 colors in order to preserve the asthetic of the GIF format. However in order to achive more smooth gradients I will allow color blending.
