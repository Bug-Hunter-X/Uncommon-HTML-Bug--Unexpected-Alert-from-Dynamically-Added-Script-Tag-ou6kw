# Uncommon HTML Bug: Dynamically Added Script Tag

This repository demonstrates a subtle but important bug related to dynamically adding script tags to an HTML document using `innerHTML`.  Dynamically adding scripts can be risky if not handled correctly. The original code demonstrates a vulnerability that leads to an unexpected alert popping up. The solution shows the safer alternative.

## Bug

The primary problem is in how the `innerHTML` is used. It can result in unexpected behavior because `innerHTML` parses the added script tag. When this tag is injected into the page the script is executed immediately causing unexpected alerts.

## Solution

The solution demonstrates a more secure approach, using `createElement` and `appendChild`. The script is added to the DOM but it will not execute unless it's also added to `document.body` or other related section.