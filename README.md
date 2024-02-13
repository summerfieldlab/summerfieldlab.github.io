# Public HIPlab Website

Hello and welcome to the new version of our public-facing website! It is viewable on the web at [https://humaninformationprocessing.com](https://humaninformationprocessing.com)

One big advantage of the new site is that it is now editable in pure Markdown + YAML. Everyone in the lab has write access to this repository and can directly make changes as needed.

**For changes to the text,** like updating "first-year DPhil student" to "second-year DPhil student", you can simply go to the relevant page --
People's bios: [/_data/people.yml](https://github.com/summerfieldlab/summerfieldlab.github.io/blob/main/_data/people.yml)
Lab publications: [/_data/publications.yml](https://github.com/summerfieldlab/summerfieldlab.github.io/blob/main/_data/publications.yml)
-- and edit it right in your browser by clicking the pencil icon in the upper-right hand corner.

**A note on YAML:** YAML can be a little bit fussy, in two ways particularly. (1) White space and indentation matters, especially around the hyphen character that represents a list item. If you're adding a new person or publication or news item, make sure to copy an existing one completely, down to the whitespace. (2) YAML does _not_ need quotation marks around strings, but it _can_ get confused when it runs into things like brackets and colons. For instance, `title: Reinforcement Learning: An Introduction` will cause a parsing error. To avoid this, you can use quotation marks like so: `title: "Reinforcement Learning: An Introduction"`.

**To add images,** you need to log into our WordPress and also size and format them correctly -- in this situation, it's best to simply send your images to Chris, who has a whole workflow for this. Once Chris has uploaded and sized the image, he can give you its URL which you can then add in the appropriate place, e.g., in the people, news, or publications YAML.

Please note that this repository, like our website itself, is public, so our edit history and discussion via issues and pull requests, etc., is by default viewable to the web, and people (if they wanted to) could fork our website codebase.
