<%*
let title = tp.file.title;
let category = "";
let tags = "";
let description = ""

function createPermalink(str) {
	return str
    .toLowerCase()
    .replace(/[^a-z0-9\s-]/g, '')
    .replace(/\s+/g, '-');
}

if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("Title");
	await tp.file.rename(title);
	category = await tp.system.prompt("Enter category (or press <RETURN> to skip)");
	tags = await tp.system.prompt("Enter tag(s) separated by commas and without `#` (or press <RETURN> to skip)");
	description = await tp.system.prompt("Enter a short description (or press <RETURN> to skip)");
}
tR += "---"
%>

title: <%* tR += title %>
date: <% tp.file.creation_date("YYYY-MM-DD") %>
draft: false
aliases: 
category: <%* tR += category %>
tags: <%* tR += tags %>
description: <%* tR += description %>
---

intro...

> [!DANGER]+ 🥱 TL;DR
> (read on for the [long version](#full-recipe))
> 1. **Start** quick recipe
> 2. **Add** step 2
> 3. etc.

## Full recipe
### Cooking time
- 10 min
### Ingredients


| Amount     |  Ingredients |
| --- | --- |
| 1   | thing    |

### Steps

### To serve
