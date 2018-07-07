# Example Website for [itty.bitty](https://itty.bitty.site)

This is a simple pure and compact [HTML](https://www.wikiwand.com/en/HTML)/[CSS](https://www.wikiwand.com/en/Cascading_Style_Sheets)/[ES5](https://www.wikiwand.com/en/ECMAScript) page intended to be compressed and encoded as an URL by **itty.bitty**

Contents is a simple converter from some [US customary units](https://www.wikiwand.com/en/United_States_customary_units) to the [metric system](https://www.wikiwand.com/en/Metric_system)

I intended to compact the HTML file quite much. I noticed many spaces can be removed in DOM element attributes, style properties, remove trailing semi-columns in style, use Linux line endings... As a result, file size is less than 1,500 bytes which is compressed under 1,200 bytes by **itty.bitty**

Style is based on [flexbox](https://www.wikiwand.com/en/CSS_flex-box_layout) layout, a little bit too large on wide screens. Using [media queries](https://www.wikiwand.com/en/Media_queries) to address this nicely would have inflated code too much

I noticed my script was not compressed correctly by **itty.bitty** when I aggressively removed semi column `;` terminators in script. I put quite all semi-columns back

I tried on mobile thru the generated [QR-code](https://www.wikiwand.com/en/QR_code). I noticed [unicode](https://www.wikiwand.com/en/Unicode) (encode in [UTF-8](https://www.wikiwand.com/en/UTF-8)) does not work well with HTML dropdown on Android (at least on my version 6)

## Quick introduction to *itty.bitty*

(*grabbed and adapted from [here](http://how.bitty.site/)*)

**itty.bitty** takes html (or other data), compresses it into a URL fragment, and provides a link that can be shared. When it is opened, it inflates that data on the receiver’s side

To fit more in the URL, the content is compressed using the [Lempel–Ziv–Markov chain algorithm](https://www.wikiwand.com/en/Lempel–Ziv–Markov_chain_algorithm). This significantly reduces the size of html, allowing for nearly a printed page worth of content.
This compressed data is [base64](https://www.wikiwand.com/en/Base64) encoded, which converts it into to a set of letters and numbers that can be included in a URL

**itty.bitty** stores this text in a section of the URL called a [fragment](https://www.wikiwand.com/en/Fragment_identifier) after the first # symbol:  `itty.bitty.site/#Name/SITE_DATA`

*Fragments* have a unique property: they are not sent to the server when requesting a website. Instead, the web browser traditionally uses them to scroll the page when it is loaded

The links that are generated from this process are complete and substantial. While most sites/apps support about 2,000 bytes, some can handle more

Once the link is sent and opened, it loads **itty.bitty.site** to reverse the process, which is done completely on device. Data are extracted, inflated, and then shown in the web browser

## Where does *itty-bitty* come from?

In English, *itty-bitty* [ĭt′ē-bĭt′ē], sometimes written *itsy-bitsy*, means very small, probably an alteration of *little bit*. The technique used here is available on GitHub at: https://github.com/alcor/itty-bitty

It has been developed by **Nicholas Jitkoff**  and published in July 2018. Nicholas, former lead designer for Google’s Material Design team for 10 years, was appointed VP of design at Dropbox in February 2017

