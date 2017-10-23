# Project 7 - WordPress Pentesting

Time spent: 4 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Cross-Site Scripting of an audio file for a Post
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.3.1
  - [X] GIF Walkthrough: <img src=' https://i.imgur.com/smlS00E.gifv' title='GIF Walkthrough' 
  width='' alt='GIF Walkthrough' /> 
  - [X] Steps to recreate: Go to add a new post and in the text format type in <HTML xmlns: ><audio>
<audio src=wp onerror=alert('XSS')>. Then click on the visual tab. A prompt box will appear with the error
XSS in it. 
  - [X] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/a493dc0ab5819c8b831173185f1334b7c3e02e36)
2. (Required) Authenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types:
    - Tested in version:4.2.2
    - Fixed in version: 4.2.3
  - [X] GIF Walkthrough: <img src=' https://i.imgur.com/MD2ZCkD.gifv' title='GIF Walkthrough' 
  width='' alt='GIF Walkthrough' /> 
  - [X] Steps to recreate: Add another post in the text format 
  Then type in <a href="[caption code=">]</a><a title=" onmouseover=alert(1)  ">http://google.com</a>.
  Post it and then go to the main page and click on the new post. Once there just put your mouse over the 
  the link and a prompt box will appear with a 1. Just hit ok to get out of it. 
  - [X] Affected source code:
    - [Link 2](https://wpvulndb.com/vulnerabilities/8111)
3. (Required) Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeded
  - [X] Summary: 
    - Vulnerability types: XSS 
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.3
  - [X] GIF Walkthrough: <img src=' https://i.imgur.com/d3Gi8Tq.gifv' title='GIF Walkthrough' 
  width='' alt='GIF Walkthrough' />
  - [X] Steps to recreate: Make a new post and in the post type in [embed src='https://youtube.com/embed/12345\x3csvg onload=alert(1)\x3e'][/embed]
  and then post it. Once you click on the the new post an error message should appear with the alert. 
  - [ ] Affected source code:
    - [Link 3](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2017] [Anajah Delestre]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.