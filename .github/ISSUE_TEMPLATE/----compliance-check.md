---
name: " \U0001F6A7 Compliance check"
about: 508/WCAG compliance check
title: Compliance check
labels: frontend
assignees: ''

---

## Why

This issue is a dev and QA checklist for section 508 compliance (which requires [WCAG 2.0](https://www.w3.org/TR/WCAG20/) A & AA). If the site in question incorporates [Platform UI](https://github.com/ritterim/platform-ui), much of the WCAG compliance is built in. These checks are required for any public-facing web property. While we try to maintain these standards behind logins as well, we are not compelled to do so.

[WCAG 2.1: all success criteria and all techniques.](https://www.w3.org/WAI/WCAG21/quickref/)

## What

### The following serves as a guide for both dev and QA

1. Text alternatives for non-text content. 
 - Do images have `alt` tags with meaningful descriptions
 - Do icons have `aria-hidden="true"` if paired with text

2. Video
  - Closed captioning (CC)
  - If only video on a page, is there a transcript or audio-only version?

3. Contrast
  - Does all text meet WCAG 2.0 AA contrast (4.5:1) requirements against white/color backgrounds and overlaid on images
  - Exceptions:
    	- Large text: contrast 3:1
    	- Incidental: Text or images of text that are part of an inactive user interface component, that are pure decoration, that are not visible to anyone, or that are part of a picture that contains significant other visual content, have no contrast requirement.
    	- Logotypes: Text that is part of a logo or brand name has no contrast requirement.
  - Tools (anyone can add to the list):
  	 - [VisBug Chrome extension](https://chrome.google.com/webstore/detail/visbug/cdockenadnadldjbbgcallicgledbeoc) 	

4. Images of Text
  - If the technologies being used can achieve the visual presentation, text is used to convey information rather than images of text except for the following:
    	- Customizable: The image of text can be visually customized to the user's requirements;
    	- Essential: A particular presentation of text is essential to the information being conveyed.

## Testing

Testing tools. 

https://www.section508.gov/test/web-software

A reliable accessibility checker you can also use is the Siteimprove Accessibility Checker. You can add it as a Chrome extension. You can configure this extension to look for WCAG A and AA errors only.

https://chrome.google.com/webstore/detail/siteimprove-accessibility/efcfolpjihicnikpmhnmphjhhpiclljc?hl=en-US
