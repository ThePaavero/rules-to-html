# Quick Rules to HTML

## The Problem
Always when building a campaign site, there will be a "rules" view of some sort.
It's usually an MS Office document that follows a certain syntax.

Manually translating the document to markup is a tedious task, especially since any
legal piece of copy tends to get updated multiple times. 

## The Solution
This tool allows you to copy the document as plain text into the left textarea and
get a best guess generated string of markup in the right textarea.

## Assumptions
The logic goes like this:
1. If the row is in ALL CAPS, wrap it into an `<h2>`
2. If the row starts with a number, followed by a period, wrap it into an `<h3>`
3. If the row starts with an asterisk, wrap it into an `<li>` (the wrapping `<ul>` will be injected)
4. All other rows are wrapped into a `<p>`
