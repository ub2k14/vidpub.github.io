---
title:  "How to create a new post!"
---
##using a Shell Script

'''sh
function new_post(){
	cd _posts 
	SLUGIFIED="$(echo -n "$1" | sed -e 's/[^[:alnum:]]/-/g' | tr -s '-' | tr A-Z a-z)"
	SLUG=$(date + "%Y-%m-%d"-$SLUGIFIED.md)
	echo -e "---\nlayout: post\ntitle: '$1'\nfeatured_image: ''\ncomments: false\ntags: \nsummary:"
	'Summary Here' \n---\n\n## Be Brilliant" > $SLUG
	echo $SLUG
	cd ../
	jekyll serve -w
}

'''


