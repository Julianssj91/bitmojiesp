## Generating and searching friendmojis

In order to use the [friendmoji generator](https://jpoles1.github.io/bitmoji/friends.html?firstid=128256895_1-s1&secondid=128257004_1_s1) you will need your ID and that of a friend (or you can use your own ID twice!). Substitute your ids in here: https://jpoles1.github.io/bitmoji/friends.html?firstid=IDHERE&secondid=IDHERE.

I got my ID by extracting it from an image URL generated by the bitmoji extension for google chrome! It seems that these IDs can take at least two different forms:
 - 128257004_1_s1
 - 934d9900-892a-4515-8beb-202d6c42a6ee


## List of bitmoji images:

Access the bitmoji list in json format [here](https://api.bitmoji.com/content/templates).

Use the entries in "imoji" for solo comics, and the entries in "friends" for friendmojis.

## Making sense of the data

* Individual comics are in .imoji (1117 of them) replace the `%s` with an avatar id
* Multi-avatar comics are in .friends (296 of them) replace both `%s` with an avatar id (eg from .imoji or .friends)
* `https://render.bitstrips.com/v2/cpanel/:comic_id-%s-v1.png?option1&option2&...`
  * `transparent=1` to set the bg to true
  * `palette=1` no idea
  * `width=200` scale image width to 200 pixels
* `https://render.bitstrips.com/render/:comic_id/%s-v1.png?option1&option2&...`
  * `cropped=%22body%22` you can also set cropped to `"head"`
  * `outfit=971786` put the user in
  * `head_rotation=1` rotate the head to position 1
  * `body_rotation=1` rotate the body to position 1
  * `pd2={"mouth":"_blank"}` inside `pd2`, you can put any of these keys: `[  "beard",  "brow_L",  "brow_R",  "cranium",  "detail_E_L",  "detail_E_R",  "detail_L",  "detail_R",  "detail_T",  "ear_L",  "ear_R",  "eye_L",  "eye_R",  "eyelash_L",  "eyelash_R",  "eyelid_L",  "eyelid_R",  "eyelines_L",  "eyelines_R",  "forehead",  "glasses",  "hair_back",  "hair_front",  "hairbottom",  "hat",  "jaw",  "mouth",  "nose",  "pupil_L",  "pupil_R",  "stachin",  "stachout",  "tongue"]`