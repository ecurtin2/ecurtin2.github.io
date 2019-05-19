
---
author: Evan Curtin
date: 2016-12-14
readingtime: 1
slug: what-is-a-molecule
tags:
- Python
- Chemistry
title: What is a molecule?

---

<div class="notebook-content">
<style type="text/css">/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area 
div.output_area 
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}



.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}






.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}








.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}





.rendered_html pre,




.rendered_html tr,
.rendered_html th,


.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}

.rendered_html * + p {
  margin-top: 1em;
}

.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,

.rendered_html img.unconfined,


.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] 
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered 
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered 
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
</style>
<style type="text/css">.highlight-ipynb .hll { background-color: #ffffcc }
.highlight-ipynb  { background: #f8f8f8; }
.highlight-ipynb .c { color: #408080; font-style: italic } /* Comment */
.highlight-ipynb .err { border: 1px solid #FF0000 } /* Error */
.highlight-ipynb .k { color: #008000; font-weight: bold } /* Keyword */
.highlight-ipynb .o { color: #666666 } /* Operator */
.highlight-ipynb .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight-ipynb .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight-ipynb .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight-ipynb .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight-ipynb .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight-ipynb .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight-ipynb .gd { color: #A00000 } /* Generic.Deleted */
.highlight-ipynb .ge { font-style: italic } /* Generic.Emph */
.highlight-ipynb .gr { color: #FF0000 } /* Generic.Error */
.highlight-ipynb .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight-ipynb .gi { color: #00A000 } /* Generic.Inserted */
.highlight-ipynb .go { color: #888888 } /* Generic.Output */
.highlight-ipynb .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight-ipynb .gs { font-weight: bold } /* Generic.Strong */
.highlight-ipynb .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight-ipynb .gt { color: #0044DD } /* Generic.Traceback */
.highlight-ipynb .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight-ipynb .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight-ipynb .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight-ipynb .kp { color: #008000 } /* Keyword.Pseudo */
.highlight-ipynb .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight-ipynb .kt { color: #B00040 } /* Keyword.Type */
.highlight-ipynb .m { color: #666666 } /* Literal.Number */
.highlight-ipynb .s { color: #BA2121 } /* Literal.String */
.highlight-ipynb .na { color: #7D9029 } /* Name.Attribute */
.highlight-ipynb .nb { color: #008000 } /* Name.Builtin */
.highlight-ipynb .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight-ipynb .no { color: #880000 } /* Name.Constant */
.highlight-ipynb .nd { color: #AA22FF } /* Name.Decorator */
.highlight-ipynb .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight-ipynb .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight-ipynb .nf { color: #0000FF } /* Name.Function */
.highlight-ipynb .nl { color: #A0A000 } /* Name.Label */
.highlight-ipynb .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight-ipynb .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight-ipynb .nv { color: #19177C } /* Name.Variable */
.highlight-ipynb .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight-ipynb .w { color: #bbbbbb } /* Text.Whitespace */
.highlight-ipynb .mb { color: #666666 } /* Literal.Number.Bin */
.highlight-ipynb .mf { color: #666666 } /* Literal.Number.Float */
.highlight-ipynb .mh { color: #666666 } /* Literal.Number.Hex */
.highlight-ipynb .mi { color: #666666 } /* Literal.Number.Integer */
.highlight-ipynb .mo { color: #666666 } /* Literal.Number.Oct */
.highlight-ipynb .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight-ipynb .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight-ipynb .sc { color: #BA2121 } /* Literal.String.Char */
.highlight-ipynb .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight-ipynb .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight-ipynb .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight-ipynb .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight-ipynb .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight-ipynb .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight-ipynb .sx { color: #008000 } /* Literal.String.Other */
.highlight-ipynb .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight-ipynb .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight-ipynb .ss { color: #19177C } /* Literal.String.Symbol */
.highlight-ipynb .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight-ipynb .fm { color: #0000FF } /* Name.Function.Magic */
.highlight-ipynb .vc { color: #19177C } /* Name.Variable.Class */
.highlight-ipynb .vg { color: #19177C } /* Name.Variable.Global */
.highlight-ipynb .vi { color: #19177C } /* Name.Variable.Instance */
.highlight-ipynb .vm { color: #19177C } /* Name.Variable.Magic */
.highlight-ipynb .il { color: #666666 } /* Literal.Number.Integer.Long */</style>
<style type="text/css">
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }
</style><script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<style type="text/css">
/* Too lazy to fix the script  just make this empty*/
</style>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>I recently replied to an reddit <a href="https://www.reddit.com/r/askscience/comments/59frj2/could_someone_explain_what_this_iupac_definition/">/r/askscience post</a> that got me overthinking about something so simple, I just had to write a post about it. The main crux of the issue is simple. At a base level, what is a molecule? As I'll show you now, a rigorous definition is a bit tricky. International Union of Pure and Applied Chemistry is basically the chemical naming authority. Here's <a href="https://goldbook.iupac.org/M04002.html">IUPAC's definition of molecule</a>:</p>
<blockquote><p>An electrically neutral entity consisting of more than one atom (n &gt; 1). Rigorously, a molecule, in which  n &gt; 1 must correspond to a depression on the potential energy surface that is deep enough to confine at least one vibrational state.</p>
</blockquote>
<p>Let's break this down into pieces</p>
<pre><code>1) An electrically neutral entity consisting of more than one atom (n &gt; 1)
</code></pre>
<p>Fair enough, if this were the whole definition then any arrangement of 2 or more atoms constitutes a molecule. This is a bit weird, considering that basically everything falls into this category, as long as it doesn't hold a charge. However there's not too much to discuss on this point.</p>
<pre><code>2) Rigorously, a molecule, in which  n &gt; 1 must correspond to a depression on the potential energy surface that is deep enough to confine at least one vibrational state.
</code></pre>
<p>What? Potential energy surface? Confined vibrations?? What does this have to do with a molecule?</p>
<p>Quite a lot actually, let's dig in!</p>
<h2 id="Potential-Energy-Surface-(PES)">Potential Energy Surface (PES)<a class="anchor-link" href="#Potential-Energy-Surface-(PES)">&#182;</a></h2><hr>
<p>We chemists like to use the phrase Potential Energy Surface a lot, so much so that we invented an acronym for it. The PES basically tells us how the energy changes as atoms move around. Let's take a look at an example PES:</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="kn">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">matplotlib</span> <span class="kn">import</span> <span class="n">animation</span><span class="p">,</span> <span class="n">rc</span>
<span class="n">rc</span><span class="p">(</span><span class="s1">&#39;animation&#39;</span><span class="p">,</span> <span class="n">html</span><span class="o">=</span><span class="s1">&#39;html5&#39;</span><span class="p">)</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="kn">as</span> <span class="nn">np</span>
<span class="k">def</span> <span class="nf">lennard_jones</span><span class="p">(</span><span class="n">r</span><span class="p">,</span> <span class="n">sigma</span><span class="p">,</span> <span class="n">epsilon</span><span class="p">):</span>
    <span class="k">return</span> <span class="mf">4.0</span> <span class="o">*</span> <span class="n">epsilon</span> <span class="o">*</span> <span class="p">((</span><span class="n">sigma</span><span class="o">/</span><span class="n">r</span><span class="p">)</span><span class="o">**</span><span class="mi">12</span> <span class="o">-</span> <span class="p">(</span><span class="n">sigma</span><span class="o">/</span><span class="n">r</span><span class="p">)</span><span class="o">**</span><span class="mi">6</span><span class="p">)</span>
<span class="k">def</span> <span class="nf">plot_pes</span><span class="p">(</span><span class="n">ax</span><span class="p">,</span> <span class="n">V</span><span class="p">):</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">r</span><span class="p">,</span> <span class="n">V</span><span class="p">,</span> <span class="n">zorder</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">(</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">(</span><span class="mf">1.4</span><span class="p">,</span> <span class="mi">3</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;Distance Between Atom Centers&#39;</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Energy&#39;</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">tick_params</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="sa">u</span><span class="s1">&#39;both&#39;</span><span class="p">,</span> <span class="n">which</span><span class="o">=</span><span class="sa">u</span><span class="s1">&#39;both&#39;</span><span class="p">,</span><span class="n">length</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_yticklabels</span><span class="p">([])</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">([])</span>
<span class="k">def</span> <span class="nf">plot_viblevels</span><span class="p">(</span><span class="n">ax</span><span class="p">):</span>
    <span class="n">r</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">500</span><span class="p">)</span>
    <span class="n">V</span> <span class="o">=</span> <span class="n">lennard_jones</span><span class="p">(</span><span class="n">r</span><span class="p">,</span> <span class="mf">1.5</span><span class="p">,</span> <span class="mf">0.9</span><span class="p">)</span>
    <span class="n">plot_pes</span><span class="p">(</span><span class="n">ax</span><span class="p">)</span>
<span class="k">def</span> <span class="nf">plot_atomsep</span><span class="p">(</span><span class="n">ax</span><span class="p">,</span> <span class="n">r</span><span class="p">):</span>
    <span class="n">circle1</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">Circle</span><span class="p">((</span><span class="mf">1.5</span> <span class="o">+</span> <span class="n">r</span><span class="o">/</span><span class="mf">2.0</span> <span class="p">,</span> <span class="mi">0</span><span class="p">),</span> <span class="mf">0.7</span><span class="p">)</span>
    <span class="n">circle2</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">Circle</span><span class="p">((</span><span class="mf">1.5</span> <span class="o">-</span> <span class="n">r</span><span class="o">/</span><span class="mf">2.0</span> <span class="p">,</span> <span class="mi">0</span><span class="p">),</span> <span class="mf">0.7</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">add_artist</span><span class="p">(</span><span class="n">circle1</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">add_artist</span><span class="p">(</span><span class="n">circle2</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">tick_params</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="sa">u</span><span class="s1">&#39;both&#39;</span><span class="p">,</span> <span class="n">which</span><span class="o">=</span><span class="sa">u</span><span class="s1">&#39;both&#39;</span><span class="p">,</span><span class="n">length</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_yticklabels</span><span class="p">([])</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">([])</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">(</span><span class="o">-</span><span class="mi">4</span><span class="p">,</span> <span class="mi">4</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">set_ylim</span><span class="p">(</span><span class="o">-</span><span class="mi">4</span><span class="p">,</span> <span class="mi">4</span><span class="p">)</span>
<span class="k">def</span> <span class="nf">plot_dot</span><span class="p">(</span><span class="n">ax</span><span class="p">,</span> <span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">r</span><span class="p">):</span>
    <span class="n">circle</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">Circle</span><span class="p">((</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">),</span> <span class="n">r</span><span class="p">)</span>
    <span class="n">ax</span><span class="o">.</span><span class="n">add_artist</span><span class="p">(</span><span class="n">circle</span><span class="p">)</span>
<span class="n">r</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">500</span><span class="p">)</span>
<span class="n">V</span> <span class="o">=</span> <span class="n">lennard_jones</span><span class="p">(</span><span class="n">r</span><span class="p">,</span> <span class="mf">1.5</span><span class="p">,</span> <span class="mf">0.9</span><span class="p">)</span>
<span class="k">def</span> <span class="nf">plot_sidebyside</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">,</span> <span class="n">idx</span><span class="p">):</span>
    <span class="n">plot_pes</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">V</span><span class="p">)</span>
    <span class="n">plot_dot</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">r</span><span class="p">[</span><span class="n">idx</span><span class="p">],</span> <span class="n">V</span><span class="p">[</span><span class="n">idx</span><span class="p">],</span> <span class="n">r</span><span class="o">=</span><span class="mf">0.05</span><span class="p">)</span>
    <span class="n">plot_atomsep</span><span class="p">(</span><span class="n">ax2</span><span class="p">,</span> <span class="n">r</span><span class="p">[</span><span class="n">idx</span><span class="p">]</span><span class="o">**</span><span class="mf">1.5</span> <span class="o">-</span> <span class="mf">1.5</span><span class="p">)</span>
<span class="n">fig</span><span class="p">,</span> <span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">)</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">ncols</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">plot_sidebyside</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">,</span> <span class="mi">125</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Here is a typical PES for a two-atom molecule such as H2 or N2. As you can see, the energy is very high towards the left, which is when we start smashing the two nuclei into one another.</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">)</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">ncols</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">plot_sidebyside</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">,</span> <span class="mi">450</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>At the other extreme on the right, the curve begins to level out. This is because the atoms are so far apart, moving them farther away does nothing, since they are completely independent.</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">)</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">ncols</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">plot_sidebyside</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">,</span> <span class="mi">170</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAd4AAAD5CAYAAACJQFT5AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMS4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvNQv5yAAAIABJREFUeJzt3Xd8XNWd9/HPGWlGvViWbEu25W7LvWAwYEKAsLQNYSGF4tCCIUueTSFPQjZl85Al2U3Cs7sJyZJQkoATIEAglJCNKQmJKcaWcS+427IsWba61TVz9o+5MsLI1tiemXtn5vt+vebl0Z1yf3dk6atz7rnnGGstIiIiEh8+twsQERFJJQpeERGROFLwioiIxJGCV0REJI4UvCIiInGk4BUREYmj9HjspLi42I4dO/Z92/bUt9PdG2LS8Nx4lCCSEFatWnXIWlvidh3HMtDPsoh80PF+luMSvGPHjqWysvJ9277429WsqWrir189Px4liCQEY8wet2s4noF+lkXkg473s+xaV3N2II22rqBbuxcREXGFi8GbTkd3r1u7FxERcYWrLd72niCaslJERFKJqy1ea6GzJ+RWCSIiInHnaosXoE3dzSIikkJcD96Obg2wEhGR1OFqVzOoxSsiIqnFveDNCLd429XiFRGRFOJe8Pqd4NW1vCIikkJcC96cjHBXc7u6mkVEJIW4FrxZAXU1i4hI6nGvxRvoa/EqeEVEJHV4oMWrrmYREUkdrl/HqxaviIikEteC15/mI5Dm03W8IiKSUlwLXghfy6uZq0REJJW4G7x+rckrIiKpxeUWb7oGV4mISEpxNXhzMtI53KXgFRGR1OFq8OZmpNGm4BURkRTibos3kK5zvCIiklJcbvGqq1lERFKL6+d4dR2viIikEndbvJnpOscrIiIpxfWu5p6gpatX53lFRCQ1uDy4KjxfswZYiYhIqnD9HC/A4U51N4uISGpwvasZ0MhmERFJGZ5o8Wpks4iIpApPBK9avCIikipcDd68TKfFq+AVEZEU4YkWr4JXRERShbuDqwJ9Xc26nEhERFKDyy3evut41eIVEZHU4Grwpqf5yEj3aXCViIikDFeDF7RCkYiIpBb3g1cLJYiISApxPXhzAgpeERFJHa4Hr7qaRUQklbgevDkZaVqdSEREUoYHglddzSIikjpcD151NYuISCpxPXhzFLwiIpJCXA/e3Ix02ruDhELW7VJERERizhPBC1qTV0REUoPrwfveCkUa2SwiIsnPA8EbXihB53lFRCQVuB68eZl9SwMqeEVEJPl5IHj9ALR29rhciYiISOx5IHjDLd7WTrV4RUQk+XkgeNXiFRGR1OGB4A23eFs61OIVEZHk53rw5gbSMUYtXhERSQ2uB6/PZ8jNSKdF53hFRCQFuB68APmZfg2uEhGRlOCJ4M3LTFdXs4iIpAQPBa9avCIikvw8Erx+WtTiFRGRFOCJ4M1Xi1dERFKEJ4I3L9Ovc7wiIpISPBK84RavtdbtUkRERGLKI8Hrpzdk6ewJuV2KiIhITHkkePsWSlB3s4iIJDdPBa9GNouISLLzRPDmZ4VXKNK0kSIikuy8Ebxak1dERFKEJ4JXa/KKiEiq8EjwqsUrIiKpwSPB65zj7VCLV0REkpsngjcnkIbPqMUrIiLJzxPBa4zRtJEiIpISPBG8oKUBRUQkNXgoeP26jldERJKeZ4K3ICtdg6tERCTpeSh4/TQreEVEJMl5JngLswI0dXS7XYaIiEhMeSd4s/00tavFKyIiyc0zwZuf5aerN0RnT9DtUkRERGLGM8FbmB2evUrneUVEJJl5JngLnKUB1d0sIiLJzDPBW5gVANTiFRGR5Oad4M3ua/FqZLOIiCQvzwRvX1ezWrwiIpLMvBO8GlwlIiIpwDPBm5eRTprPaHCViIgkNc8ErzGG/Mx0tXhFRCSpeSZ4AQqzAzQpeEVEJImlu11Af/lZfo1qFhHxoO7eEJtqWth6oJX2rl4skOVPY3xJLjNHFpAVSBv0Pay17DjYxsb9zTR39NAbtGT4fZQVZDF7dCFFOYHYH4gHeCp4CxW8IiKe0djWzWMr9vLypgNsqmmhuzc04PPSfYZJw/M4b0oJN5w1htKCrCOP9QRDPL9mP8+uqWZtVdNx110vL8pmwbgirj9rDLNGFUb9eLzCW8Gb7Wd3fZvbZYiIpLSqhnZ+/tcdPPNONR0RzJ/fG7Jsrmlhc00LD/5tJ5fNLOWms8fy5o5DLHlrD3WtXRHtd29DO3sb2nlq1T5OHzuEz547gQunDT/Vw/EcTwVvQZZWKBIRcdOTK6v4zgsbaes+uQVrekOW59fu5/m1+0+pjpW7G1m5u5LLZ5fxvStnkJ/pP6X385KIBlcZY542xvy9MSamg7EKs/y0dPYQCtlY7kZERI7S0tnD5x5dxZ1Przvp0I2FF9bu59IfLaNyd4PbpURNpEH6M+A6YJsx5vvGmIpYFFOQHcBaaD3OOQAREYmu5vYeFj34Nn9cX+t2KQOqbupg0UNv89etB90uJSoiCl5r7SvW2kXAPGA38LIx5k1jzM3GmKi1/zVtpIhIfHX2BLnp4RWsr252u5Tj6uoNcduSyqRo+UbcdWyMGQrcBCwGVgM/JhzEL0ermMK+pQE7NLJZRCQevvLUWlbvbXK7jIh09Ya4dUkl+5s63C7llER6jvcZYBmQDVxurf2YtfYJa+3ngdxoFdO3QlFDm4JXRCTWlm6s5Q/ratwu44Q0tvfw7ec2ul3GKYm0xftTa+00a+2/W2vf912y1s6PVjF9F0836lpeEZGYauvq5a7nEzPAXtl8gKUbvXk+OhKRXk5UaIy56qhtzcB6a21dtIrpC96GNp3jFRGJpXtf3UZNc6fbZZy0u57fyIcnl5DpH3zGLK+JtMV7C/AQsMi5PQh8GXjDGHN9tIrJz/ST5jM0qqtZRCRmOnuCPL5ir9tlnJKa5s6EbfVGGrwhYKq19uPW2o8D04AuYAHwtagV4zMMyfZTr+AVEYmZP22oPe7UjYniycoqt0s4KZEG71hr7YF+X9cBk621DUBU+4WHZAfU4hURiaEnViZmYB3tzR31VDW0u13GCYs0eJcZY/5gjLnRGHMj8BzwN2NMDhDVcehFOQGNahYRiZH27l7e3lXvdhlRYS289m7UhhnFTaSDq/4PcBVwDmCAJcDT1loLnB/NgopyAmyrOxzNtxQREcfmmlaSaVbeTTUtbpdwwgYNXmNMGrDUWnsh8HSsC1KLV0QkdhIxqI5nU02r2yWcsEG7mq21QaDdGFMQh3ooygnQ1N5NMJn+JBMR8Yh3a5MreN+tbSHc+Zo4Iu1q7gTWG2NeBo4smGut/UK0CyrKCRCy4fma+67rFRGR6GhMsqVXO3tCdPWGEup63kiD90XnFnPvTaLRreAVEYmynt6Q2yVEXXcwCYPXWvuIMSYLKLfWvhvLgjRtpIhI7PjTYrqsuiv8vsQ6pkgXSbgcWAP8yfl6jjHm+VgUNCQ7HLz1hxW8IiLRlpsRaUdnYvCnGTLSkzB4gbuAM3Cu2bXWrgHGxaIgtXhFRGJn0vCoLSjnCRNKcvH5jNtlnJBIg7fXWnv0KskxGUbW/xyviIhE17SyfLdLiKpEPJ5I+xw2GGOuA9KMMZOALwBvxqKgTH8a2YE0Ba+kDGstbd1BDrZ2uV2KpIDppXG5MjRuppUmb/B+Hvgm4YURHgeWAnfHqihNoiHJIhiyHDrcRW1zJ7Utne//t7mTAy3hr9u7g26XKimiINvPjJH5bKhOjut5F04sdruEExbpqOZ2wsH7zdiWE6bglUTRGwxR09xJVUM7VY3tVDV0UNXYzr7GDvY3dVDX2vWByWD8aYZheZmMKMhkalk+51cMY1heBiV5GXz8By4diKSUT80fzYbqjW6XccpmjSpgarK2eI0xk4GvAGP7v8Zae0EsihqaE6BO3W7iEV29QfbWt7PjYBs7Dx1m96G2IwFb09z5vmBN8xlKCzIZPSSbsycUU1qQyfCCTEbkZ4bv52cyNCeQcINBJLlcMWck33txM10Jfk3vp+aPdruEkxJpV/NTwM+Bh4CY94kV52Yk3Xyi4n1N7d1sqW1lx8HD7DzYxs6Dh9l5qI2qhvb3TSpfnJtBeVEWp40Zwugh2YwuynL+zaa0IJP0JLxOUpJLQZafy2eX8btV+9wu5aTlZabzsTllbpdxUiIN3l5r7c9iWkk/JXkZHDrcTShk1TKQqOsJhth1qI3NNS1srmllS20LW2paqW3pPPKcTL+PccW5zBhZwBWzyxhfksv4khzGFeeQl+l3sXqR6Ljzkiks3VhLa2ev26WclDsvnkJ+gv4sRhq8LxhjPgf8nvAAKwCstQ2xKKokL4NgyNKk+ZrlFPUEQ7xb28q6fc2srWpifXUz2+sO0x0Md7H50wwTSnI5a8JQKkbkMWVEHhOH5VJWkKU/+iSpDcvL5M6Lp/AvzyXeud45owtZtGCM22WctEiD90bn36/222aB8dEtJ6wkLwOAg61dCl6JmLWWvQ3trKlqYk1VE2urmti4v+XIeazCbD8zRxbwocljmToin4rSPMYX5xJIsFlvRKJl0YIxPLdmP5V7Gt0uJWKBdB//duXMhP7DONJRzTGZpepYSnLfC94pI/LiuWtJIKGQZVvdYVbsquftXQ2s2NVwZFBept/HzJEFfPrMMcweXcjsUQWUF2VjTOL+sIpEm89n+Pn1p3HlfW9Q1dDhdjmDMgb+45OzE3LSjP6OG7zGmDuttT907n/SWvtUv8f+zVr7jVgUdaTFe7hzkGdKKrHWsvXAYZZtO8jynQ1U7mmgyVnibER+JmeOH8oZ44qYVz6EycNzNchJJALFuRn85pYFXPPAcmqavfs71xj41ytmcPnsxBxQ1d9gLd5rgB86979OeHRzn0uA2AavLilKeY1t3SzbfohlWw+ybNuhIwOgxg7N5qJpwzlj3FAWjCti1JAstWZFTtKYoTk8cdtZfO6xVZ6cWCMnkMZ3r5zBlXNHuV1KVAwWvOYY9wf6OmpyM9LJ9PsUvCnIWsuW2laWbqzlL1vqWFfdjLXhyx/OmVjMuZOL+dCkEsoKs9wuVSSplA/N5pnbF/IfL73LA8t2YmMyG/+Jmz2qgB9fM5exxTlulxI1gwWvPcb9gb6OGmMMxbnhS4ok+QVDllV7GnlpYy0vbTrA3oZ2jAmPXPziRyZx7uQSZo8qJC2BB1OIJIJAuo+vXzaV8yuG8aNXtrJ858lduDK9LJ/rziinck8jf1i3n57gicfF8PwMbl44jlvOGZd0awgPFryzjTEthFu3Wc59nK8zY1lYSV6GWrxJLBSyrNzdwLNr9vPSxlrq27oJpPlYOHEot583gY9MHcawvJj+FxORYzhz/FB+e9tZbKhu5pev7+KVzQdoGeR63+xAGgsnFvOZheM4a8JQABadOYZ/vrSCR97czbOrq9k/yDnkdJ9h5qgCbjhrDB+dVZZ0gdvnuMFrrU2LVyFHK8nNYE99u1u7lxiw1rK5ppXn1lbzwpr97G/uJDuQxkemDufi6cP58OQSTU4h4iEzRhbwn1fPwVrLzkNtrNnbxNYDrbR3B7FYMtPTmDAslzmjC5k8PG/AXqnh+ZnceUkFd15SQV1LJ6urmthQ3UxLRw89ofB7lBZkMqe8kBllBWQFXIuduIn0Ot64K8nLSKhry+TYGtq6eeadfTxZWcXWA4dJ9xnOnVzC1y6t4O+mDSc74Nn/hiJC+PTfhJJcJpTkntL7DMvP5OLpI7h4+ogoVZaYPPsbryQvg4a2bnqCoaTtbkhmoZDlrZ31PL5iLy9tPEB3MMTc8kLu/ocZ/P3MUk2MIiIpy9PBC1B/uJsRBTrXlyia23t4fOVeHl+xlz317RRk+Vl0ZjnXnF6uyVBERPBy8PabvUrB6307Dx7mV2/s5ner9tHRE+SMsUXcceFkLpkxgkx/8p+zERGJlHeD932zVxW4W4wMyFrL8p0NPLRsJ39+tw6/z8fH5pTxmYXjEn5KNxGRWPFs8Pa1cmubdUmR11hr+du2Q9z76jZW7WlkaE6Az18wiU+fWa5LgEREBuHZ4C3JzcBnoLbZ+xN3pwprLa9uruMnf97G2n3NlBVkcvcV0/nk/NHqThYRiZBngzc9zcewvExPT9qdKvpauPcs3cKG6hZGF2Xx/atmctW8UVpST0TkBHk2eCHc3dw3Kb64Y21VEz/40xbe3FHP6KIs7vnELP5h7khd4iUicpI8HbylBZlsqzvsdhkpaU99Gz9c+i4vrquhKCfAXZdP47oFY9TCFRE5RZ4O3hEFmSzbdsjtMlJKe3cv9/1lBw/8bSdpPsMXLpjIreeO11SOIiJR4u3gzc/kcFcvrZ09+sUfY9Za/ri+lu+9uIn9zZ1cOXck/3xpBcPzNUpZRCSavB28Ry4p6lTwxtDOg4f51rMbeHNHPVNL8/nxtXM5fWyR22WJiCQlTwdvaUF4sfOa5k4mDdd0g9HWGwzx0Ou7+K+XtxJI93H3FdO5bsEYrXsrIhJDHg/e91q8El2b9rdw59Nr2VDdwsXTh3P3FTMYpm5lEZGY83TwDssPTxupa3mjpycY4ievbuO+13ZQmB3gZ4vmcenMUrfLEhFJGZ4O3oz0NIpzA9S2aPaqaNh1qI0vPbGGtVVNXDVvJN/+6DQKs7U8n4hIPHk6eCE8wEot3lNjreXJyiq+88Im/Gk+7ls0j8vUyhURcYX3gzc/i6qGdrfLSFhN7d3889Pr+dPGWs6eMJT/+NTsI4PWREQk/jwfvKOGZPHWjkNYazFGo21PxIbqZv7xN6s40NLJNy6rYPE54/FpxLKIiKsSInjbuoM0tvdQlKPzkZF6YuVe/uW5jRTnBHjys2cxt3yI2yWJiAgJELyji7IBqGpoV/BGoLMnyLef28CTlfv40KRifnzNXH1uIiIe4v3gHeIEb2M7s0cXulyNt9U0d3Drkko2VLfwhQsm8sULJ2syDBERj/F+8BaFBwJVNeiSouNZt6+JxY9U0t4d5Bc3zucjU4e7XZKIiAzA88Gbl+mnMNtPVaNGNh/LH9fX8OUn11Ccm8Gvb1nAlBGaXlNExKs8H7wQ7m7WJUUfZK3lvtd2cM/Sd5lXXsgDN8ynODfD7bJEROQ4EiN4i7LYUtPqdhme0hsM8Y3fr+fJyn1cMaeMH3x8Fpn+NLfLEhGRQfjcLiASo4dks6+xg1DIul2KJ3T2BLn90Xd4snIfn79gIj+6eo5CV0QkQSREi3dUUTbdwRB1rV1H1uhNVS2dPSx+pJIVuxq46/Jp3LRwnNsliYjICUiM4B3ijGxubE/p4D3Y2sWNv1zB1gOt/PiaOVwxZ6TbJYmIyAlKiK7mcmcSjT31qTvAqrqpg0/8/E12HWrjFzedrtAVEUlQCdHiHT0kmzSfYdehw26X4oqqhnaufXA5zR09PHrrAuZp+kcRkYSVEMEbSPdRXpTNzoNtbpcSd1UN7VzzwHJaO3t4dPECZo3S7F0iIoksIYIXYHxxTsoF7576Nq59YDlt3UEeu/VMZowscLskERE5RQlxjhdgfEkOu+rbCKbIJUW7D7VxzQPL6egJ8titCxS6IiJJIoGCN5fu3hD7m5J/zubqpg6ue3A5Xb0hHrv1TKaXKXRFRJJF4gRvcQ4AOw8ld3fzwdYuPv3Q27R29fLrW85gamm+2yWJiEgUJUzwjitxgvdg8o5sbm7v4fpfvE1tcycP33y6WroiIkkoYYK3JDeDvIz0pB1g1dbVy00Pr2DnwTYevGE+p40pcrskERGJgYQZ1WyMYXxJDjuT8Frezp4gty6pZN2+Zu5bNI9zJhW7XZKIiMRIwrR4ASaU5LK9LrmCNxSy/N8n1/Lmjnru+cQsLp4+wu2SREQkhhIqeKeMyONASxeNbd1ulxI1//bHzby4voZvXjaVq+aNcrscERGJsYQK3r4RvptrW1yuJDp+8fouHnp9FzedPZbFH9IqQyIiqSChgreiNA+ALTWtLldy6l5cV8N3X9zEJdNH8C8fnYYxxu2SREQkDhIqeIflZVKcG2BzTWK3eFfsauCOJ9dwWvkQfnTNHNJ8Cl0RkVSRUMELUDEiny21idvi3V53mFuXVDJqSBYP3jCfTH+a2yWJiEgcJWDw5rH1QCu9wZDbpZywxrZubnlkJek+wyM3n8GQnIDbJYmISJwlXPBOLc2nqzfE7vrEmkijJxji9kdXUdPUyQM3nMboomy3SxIRERckXPD2DbDalEADrKy1fPu5jSzf2cD3Pz5Ts1KJiKSwhAveScPyCKT7WFfV5HYpEXv4zd08vmIvt583QdfqioikuIQL3kC6j5kjC1idIMH72rt13P2HTVw0bThfvWiK2+WIiIjLEi54AeaOLmRDdTPdvd4eYLW9rpXPP7aaKSPy+a+r5+DTZUMiIikvIYN3TnkhXb0htnh4BqvwCOZKMvw+HrpxPjkZCbMehYiIxFBCBu/c8iEArPFod3P/Ecz3Xz+fkYVZbpckIiIekZDBW1aQybC8DFbv9Wbw/usLm/qNYB7idjkiIuIhCRm8xhjmlheyem+j26V8wGNv7+XXy/dw27njNYJZREQ+ICGDF+D0sUXsrm+nprnD7VKOWLGrgW8/t4EPTy7ha5dUuF2OiIh4UMIG78KJxQC8sb3e5UrC9jW2c/tvVlFelM29187VwgciIjKghA3eKcPzKM4N8Mb2Q26XQnt3L7ctWUV3b4gHb5xPQZbf7ZJERMSjEjZ4fT7D2ROKeX37Iay1rtVhreWrT61jc20L9147lwklua7VIiIi3pewwQuwcOJQDrZ2sb3usGs1/PdftvPi+hq+dkkF51cMc60OERFJDAkevOHzvH/detCV/b+86QD//6Wt/MOcMj577nhXahARkcSS0ME7akg2FSPyWLqxNu773naglTueWMOsUQV8/+OzMEaDqUREZHAJHbwAl84opXJPI3UtnXHbZ2NbN4uXVJLpT+P+608j058Wt32LiEhiS/zgnTkCa4lbq7ezJ8htv66kprmT+68/jdICTQcpIiKRS/jgnTQsl/ElOfzPhtgHr7WWO3+3jpW7G/nPT83WdJAiInLCEj54jTF8dGYpy3fWs78ptrNY/dfLW3l+7X7uvGQKH51VFtN9iYhIckr44AX45PzRWOC3K/bGbB9PVVZx75+3c/X80dz+4Qkx24+IiCS3pAje0UXZnDe5hN+urKInGIr6+7/2bh1ff2Y9CycO5btXztAIZhEROWlJEbwAixaMoa61i5c3HYjq+67Y1cA//mYVk4fncd+i0/CnJc1HJiIiLkiaFDm/YhjlRdnc99r2qE0huX5fM595eCVlhVksueUMzcEsIiKnLGmCN81n+KcLJrKhuoVXNted8vtt2t/Cjb9aQUGWn0cXL6A4NyMKVYqISKpLmuAFuGruSMaX5PC9FzfR1Rsc8DmRtIYrdzdw9QNvkZnu49HFC3StroiIRE262wVEU3qaj7sun84Nv1zBf/95O1++aAqdPUFeXFfDc2v3s2JXPZ09IQqy/FxQMYwr5pRx3pT3L2zw2rt13P6bdygtyOTXixcwslChKyIi0ZNUwQtw7uQSrpo3kp/+ZTvjinO477UdbDtq9aLmjh5+v7qa36+u5sKpw7n32jlk+dO4/287+eGftjBlRD5LPnMGJXnqXhYRkehKuuAFuPuKGazZ28SXn1zLYB3Lr2w+wG1LVpGTkcbSjQe4bOYI7vnEbHIykvKjERERlyXVOd4+ORnpXDR9+KCh2+f17Yd4dXMd37isgv++bp5CV0REYiZpE+aP609s7uYLKoZx27makUpERGIrKVu8EF6670QEQ9G59ldEROR4kjZ4y05wNHJpYWaMKhEREXlP0gbvzQvHRvxcn4Gbzo78+SIiIicraYP3qnmjmF6WH9Fzr1tQzsRheTGuSEREJImDN5Du47HFZ3L+lJJjPscY+OyHx/OvH5sRx8pERCSVJe2oZoCCbD+/uvkM1u1r4tnV+1mxu56O7iCF2QEuqBjGx2aXMboo2+0yRUQkhSR18PaZNaqQWaMK3S5DREQkebuaRUREvEjBKyIiEkcKXhERkThS8IqIiMSRiWRh+FPeiTEHgT0x35FI4htjrT32NXAu08+ySMSO+bMcl+AVERGRMHU1i4iIxJGCV0REJI4UvCIiInGk4BUREYkjBa+IiEgcKXhFRETiKGGD1xgTNMasMcZsNMasNcZ82Rjjcx6bb4y59zivHWuMuS5+1X5g/321rzXGvGOMOXuQ5xcaYz4Xr/oGY4z5sTGmuu/zdradN9hxnML+/MaY7xtjthljNhhjVhhjLj3J94pZnSIikUjY4AU6rLVzrLXTgb8DLgP+H4C1ttJa+4XjvHYs4Frw8l7ts4GvA/8+yPMLAU8ErxO2VwJVwLn9HjoPiFWg3Q2UAjOstTOAy4G8k3yv8zjBOo0xKbGKl4jEibU2IW/A4aO+Hg/UA4bwL9c/ONs/DKxxbqsJ/8JeDjQ72+4gHMTLgHec29nOa88DXgN+B2wBHuW9SUdOB94E1gIrnPdNA+4BVgLrgM8OVjvwSeDZfl9/td/rv+Ns+y3Q4dR7D3Af8DHnsd8Dv3Tu3wJ817n/aaeuNcD9QJqz/SLgLec4nwJyne27ge8429cDFceo/SPAH4EbgfudbWOBWqDa2d+HgDHAq85xvAqUO899GPgZ8Bdgp/P9+SWwGXh4gP1lO9/X/GPUE/HxHKPOEuBp5zNfCSx0Xn8X8ADwEvAYML3f57kOmOT2z4BuuumWmDfXCzjpwo8KXmdbIzCc9wfvC/1+meYSXoP4yOPO9mwg07k/Cah07p9HOKBHEe4deAs4Bwg4oXG687x8531vA77lbMsAKoFxA9QZdH6Bb3He/zRn+0XOL3vj7O8PhFuVY4EN/V5/DXCPc38FsNy5/yvgYmCqc9x+Z/t9wA1AMfA3IMfZ/jXg28793cDnnfufAx46xuf+EHC9c8zV/fZxF/CVfs97AbjRuf8ZnD8uCAfvb51jvAJoAWY6x7sKmHPU/mYBq49RywkfzwB1Pgac49wvBzb3e94qIMv5+ifAIud+oG+7brrpptuJ3pKtC80MsO0N4D+NMY8Cz1hBlUAZAAADqUlEQVRr9xnzgaf5gZ8aY+YQDsXJ/R5bYa3dB2CMWUM4BJuBGmvtSgBrbYvz+EXALGPMJ5zXFhAO8l1H7a/DWjvHec1ZwBJjzAzCwXsR4ZY5hP9QmATsPer1y4AvGWOmAZuAIcaYUuAs4AuEW6OnASudY80C6oAzgWnAG872AOE/Jvo84/y7Crjq6A/JGBMg3KV/h7W21RjztlPvi0c/16ml7z1+Dfyw32MvWGutMWY9cMBau955/42EP981A7zfQE7peBwXAtP6/Z/IN8b0dWM/b63tcO6/BXzTGDOK8P+jbRHWKCLyPkkTvMaY8YRDs45wiw8Aa+33jTEvEg6M5caYCwd4+R3AAWA24ZZXZ7/HuvrdDxL+zAww0CTXhnAra2mkdVtr3zLGFBPu8jTAv1tr7z/q2MYe9ZpqY8wQ4BLCLb4i4FOEewFaTThFHrHWfv2o97kceNlae+0xyuk71r7jPNolhP+YWO8EVTbQzsDB+4FDHWA/Id7/+YYG2O92oNwYk2etbT3qMcOpHQ+Ev99n9QvY8BuHj6/tSPHWPub8ofH3wFJjzGJr7Z+P8Z4iIseUyIOrjjDGlAA/B35qrbVHPTbBWrveWvsDwl2/FUAr7x+cU0C4BRsi3I2aNsgutwBlxpjTnX3kOQNwlgK3G2P8zvbJxpicQWqvcPZX77z+M8aYXOexkcaYYQPUC+EW2JcIB+8y4CvOvxA+p/oJ57UYY4qMMWMIn9teaIyZ6GzPNsZMJnLXAouttWOttWOBccBFxpjsAWp8k3CXOMAi4PUT2M8R1tp24BfAvU6LG2NMqTHm0yd5PEfX+RLwT31fOL0eH+D8YbfTWnsv8DzhLnARkROWyMGb1Xc5EfAK4V+g3xngeV9yLkFZS3iA0v8QHhzT61zOcwfhc6A3GmOWE+5mbhvgfY6w1nYDVwM/cd73ZSCT8PnPTcA7xpgNhAc1DdTS6qt9DfAE4XOhQWtt30Cet5xu2N8BedbaesLdqRuMMfc477EMSLfWbic8gKjI2Ya1dhPwLeAlY8w6p75Sa+1B4CbgcWf7csJ/iAzKCdeL6de6tda2EQ7Uywmf073SOa4PEe7yvtnZz/XAFyPZzzF8CzgIbHI+12eBgyd5PAPVOd8Ys84Yswn4x2O87mpgg/M9qwCWnMLxiEgK07KAIiIicZTILV4REZGEo+AVERGJIwWviIhIHCl4RURE4kjBKyIiEkcKXhERkThS8IqIiMSRgldERCSO/hdI4aNpa3/VxwAAAABJRU5ErkJggg==
"
>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Lastly, we have the case where the atoms are in their lowest energy arrangement. Since nature likes moving towards a low energy state, this is the most stable form of the molecule. The distance at which this occurs is the <strong>bond length</strong>.</p>
<p>So, we can think of a molecule forming from atoms <strong>when the lowest energy point of the PES is not the atoms being far apart</strong>. An example where this might not happen is in the following PES:</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">ncols</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">4</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">V2</span> <span class="o">=</span> <span class="mi">1</span><span class="o">/</span><span class="p">(</span><span class="n">r</span> <span class="o">-</span> <span class="mf">0.8</span><span class="p">)</span> <span class="o">-</span> <span class="mi">1</span>
<span class="n">plot_pes</span><span class="p">(</span><span class="n">ax</span><span class="p">,</span> <span class="n">V2</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Notice how the energy keeps going down as you increase the distance. This means that the atoms will constantly want to keep getting farther apart, and <strong>you have no molecule!</strong> In the words of IUPAC, a surface that looks like this has no depression whatsoever!</p>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Vibrational-State">Vibrational State<a class="anchor-link" href="#Vibrational-State">&#182;</a></h2><hr>
<p>Ok so we've learned that in order to have a molecule, we need to have a PES with a <em>depression</em> in it. Most of the time we call such a depression a <strong>potential well</strong>. This is because a potential well is lower than the points around it, much like a regular well. However, atoms in molecules are always vibrating about. What does this mean for our molecules' existance? It means that the vibration can't have too much energy, or else the molecule will <strong>tear itself apart</strong>. Let's draw some pictures to clarify.</p>
<p>Here is what it would look like for a molecule to be safely vibrating, but still staying together:</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">from</span> <span class="nn">matplotlib.animation</span> <span class="kn">import</span> <span class="n">FuncAnimation</span>
<span class="n">fig</span><span class="p">,</span> <span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">)</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">ncols</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">nframes</span> <span class="o">=</span> <span class="mi">120</span>
<span class="k">def</span> <span class="nf">animate</span><span class="p">(</span><span class="n">i</span><span class="p">):</span>
    <span class="n">ax1</span><span class="o">.</span><span class="n">clear</span><span class="p">()</span>
    <span class="n">ax2</span><span class="o">.</span><span class="n">clear</span><span class="p">()</span>
    <span class="n">r</span> <span class="o">=</span> <span class="mf">1.76</span> <span class="o">+</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">i</span> <span class="o">*</span> <span class="mi">2</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">pi</span> <span class="o">/</span> <span class="mi">60</span><span class="p">)</span> <span class="o">*</span> <span class="mf">0.2</span>  <span class="c1"># 60 frames per cycle</span>
    <span class="n">_</span> <span class="o">=</span> <span class="n">plot_pes</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">V</span><span class="p">)</span>
    <span class="n">_</span> <span class="o">=</span> <span class="n">plot_dot</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">r</span><span class="p">,</span> <span class="n">lennard_jones</span><span class="p">(</span><span class="n">r</span><span class="p">,</span> <span class="mf">1.5</span><span class="p">,</span> <span class="mf">0.9</span><span class="p">),</span> <span class="n">r</span><span class="o">=</span><span class="mf">0.05</span><span class="p">)</span>
    <span class="n">_</span> <span class="o">=</span> <span class="n">plot_atomsep</span><span class="p">(</span><span class="n">ax2</span><span class="p">,</span> <span class="n">r</span><span class="o">**</span><span class="mf">1.5</span> <span class="o">-</span> <span class="mf">1.5</span><span class="p">)</span>
<span class="n">ani</span> <span class="o">=</span> <span class="n">FuncAnimation</span><span class="p">(</span><span class="n">fig</span><span class="p">,</span> <span class="n">animate</span><span class="p">,</span> <span class="n">interval</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span> <span class="n">frames</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">nframes</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
<span class="n">ani</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[5]:</div>
<div class="output_html rendered_html output_subarea output_execute_result">
<video width="576" height="288" controls autoplay loop>
  <source type="video/mp4" src="data:video/mp4;base64,AAAAHGZ0eXBNNFYgAAACAGlzb21pc28yYXZjMQAAAAhmcmVlAAA2q21kYXQAAAKuBgX//6rcRem9
5tlIt5Ys2CDZI+7veDI2NCAtIGNvcmUgMTQ4IHIyNjQzIDVjNjU3MDQgLSBILjI2NC9NUEVHLTQg
QVZDIGNvZGVjIC0gQ29weWxlZnQgMjAwMy0yMDE1IC0gaHR0cDovL3d3dy52aWRlb2xhbi5vcmcv
eDI2NC5odG1sIC0gb3B0aW9uczogY2FiYWM9MSByZWY9MyBkZWJsb2NrPTE6MDowIGFuYWx5c2U9
MHgzOjB4MTEzIG1lPWhleCBzdWJtZT03IHBzeT0xIHBzeV9yZD0xLjAwOjAuMDAgbWl4ZWRfcmVm
PTEgbWVfcmFuZ2U9MTYgY2hyb21hX21lPTEgdHJlbGxpcz0xIDh4OGRjdD0xIGNxbT0wIGRlYWR6
b25lPTIxLDExIGZhc3RfcHNraXA9MSBjaHJvbWFfcXBfb2Zmc2V0PS0yIHRocmVhZHM9NiBsb29r
YWhlYWRfdGhyZWFkcz0xIHNsaWNlZF90aHJlYWRzPTAgbnI9MCBkZWNpbWF0ZT0xIGludGVybGFj
ZWQ9MCBibHVyYXlfY29tcGF0PTAgY29uc3RyYWluZWRfaW50cmE9MCBiZnJhbWVzPTMgYl9weXJh
bWlkPTIgYl9hZGFwdD0xIGJfYmlhcz0wIGRpcmVjdD0xIHdlaWdodGI9MSBvcGVuX2dvcD0wIHdl
aWdodHA9MiBrZXlpbnQ9MjUwIGtleWludF9taW49MjUgc2NlbmVjdXQ9NDAgaW50cmFfcmVmcmVz
aD0wIHJjX2xvb2thaGVhZD00MCByYz1jcmYgbWJ0cmVlPTEgY3JmPTIzLjAgcWNvbXA9MC42MCBx
cG1pbj0wIHFwbWF4PTY5IHFwc3RlcD00IGlwX3JhdGlvPTEuNDAgYXE9MToxLjAwAIAAAA0HZYiE
ADP//vbsvgU1/Z/QlxEsxdpKcD4qpICAdzTAAAADAAADAACG7EIUw97UeeSAAACuk6DvcSW+ABGL
RdQuyaW+kpHvO2xjSSJLw/WLJN8d07jpNfwG5ibC4aGII6t839xvamLnB6cqclmRyXrXy+l3PHuJ
o6HJBZVosPVXKutlwvnDUlYbMlUbxxCWYnJG97PQaQac/N0E96YCXxWHO8zQncZLAYEstp0hc9fG
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
AAAcdXVpZGtoQPJfJE/FujmlG88DI/MAAAAAAAAAGHN0dHMAAAAAAAAAAQAAAHgAAAEAAAAAFHN0
c3MAAAAAAAAAAQAAAAEAAAPQY3R0cwAAAAAAAAB4AAAAAQAAAgAAAAABAAAFAAAAAAEAAAIAAAAA
AQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAAB
AAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEA
AAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAA
AQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAA
AAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIA
AAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAA
AAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAACAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAA
AAEAAAEAAAAAAQAAAgAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAA
AQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAAB
AAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEA
AAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAA
AAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAAC
AAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUA
AAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAA
AAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAA
AAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAA
AQAAAAAAAAABAAABAAAAAAEAAAIAAAAAHHN0c2MAAAAAAAAAAQAAAAEAAAB4AAAAAQAAAfRzdHN6
AAAAAAAAAAAAAAB4AAAPvQAAAYMAAABcAAAAQQAAADoAAAEgAAAAQgAAADwAAAAfAAAAlQAAADwA
AAApAAAAIAAAAGQAAAAjAAAAIQAAABUAAAB7AAAAKwAAACEAAAAkAAAAzgAAAD4AAAAsAAAAJgAA
AIwAAAA7AAAAIwAAADkAAADHAAAATQAAADAAAAA3AAAAnAAAAE0AAAA2AAAAMAAAANwAAABSAAAA
OwAAADwAAADdAAAALQAAACkAAAAgAAAATQAAACMAAAAgAAAAIAAAAHwAAADJAAAARgAAACoAAAA5
AAAAuAAAAMAAAABIAAAANwAAAC8AAAErAAAATQAAADYAAAAwAAAAuAAAAD4AAAAuAAAAJgAAAQQA
AAA/AAAAJgAAADEAAACCAAAAMAAAAB4AAAAdAAAASAAAACQAAAAXAAAAHQAAAJ4AAAA3AAAAHwAA
ACcAAACMAAAAQwAAACcAAAAqAAAAywAAAEgAAAA7AAAAMwAAAKsAAABRAAAANwAAAC4AAAC5AAAA
VQAAADoAAAA5AAAAswAAAFQAAAAzAAAAHAAAAFgAAAAkAAAAJQAAABwAAACWAAAAKQAAACkAAAAg
AAAArwAAAEoAAAAyAAAAMgAAAI8AAABUAAAAKwAAADUAAABeAAAAFHN0Y28AAAAAAAAAAQAAACwA
AABidWR0YQAAAFptZXRhAAAAAAAAACFoZGxyAAAAAAAAAABtZGlyYXBwbAAAAAAAAAAAAAAAAC1p
bHN0AAAAJal0b28AAAAdZGF0YQAAAAEAAAAATGF2ZjU2LjQwLjEwMQ==
">
  Your browser does not support the video tag.
</video>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>And here is what it would look like if the molecule's vibration had so much energy that it fell apart!</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">ax2</span><span class="p">)</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">nrows</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">ncols</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">nframes</span> <span class="o">=</span> <span class="mi">120</span>
<span class="n">V3</span> <span class="o">=</span> <span class="n">lennard_jones</span><span class="p">(</span><span class="n">r</span><span class="p">,</span> <span class="mf">1.5</span><span class="p">,</span> <span class="mf">0.1</span><span class="p">)</span>
<span class="k">def</span> <span class="nf">animate</span><span class="p">(</span><span class="n">i</span><span class="p">):</span>
    <span class="n">ax1</span><span class="o">.</span><span class="n">clear</span><span class="p">()</span>
    <span class="n">ax2</span><span class="o">.</span><span class="n">clear</span><span class="p">()</span>
    <span class="n">r</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mf">1.5</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="n">nframes</span><span class="p">)[</span><span class="n">i</span><span class="p">]</span>
    <span class="n">plot_pes</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">V3</span><span class="p">)</span>
    <span class="n">plot_dot</span><span class="p">(</span><span class="n">ax1</span><span class="p">,</span> <span class="n">r</span><span class="p">,</span> <span class="n">lennard_jones</span><span class="p">(</span><span class="n">r</span><span class="p">,</span> <span class="mf">1.5</span><span class="p">,</span> <span class="mf">0.1</span><span class="p">),</span> <span class="n">r</span><span class="o">=</span><span class="mf">0.05</span><span class="p">)</span>
    <span class="n">plot_atomsep</span><span class="p">(</span><span class="n">ax2</span><span class="p">,</span> <span class="n">r</span><span class="o">**</span><span class="mf">1.5</span> <span class="o">-</span> <span class="mf">1.5</span><span class="p">)</span>
<span class="n">ani</span> <span class="o">=</span> <span class="n">FuncAnimation</span><span class="p">(</span><span class="n">fig</span><span class="p">,</span> <span class="n">animate</span><span class="p">,</span> <span class="n">interval</span><span class="o">=</span><span class="mi">20</span><span class="p">,</span> <span class="n">frames</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">nframes</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
<span class="n">ani</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[6]:</div>
<div class="output_html rendered_html output_subarea output_execute_result">
<video width="576" height="288" controls autoplay loop>
  <source type="video/mp4" src="data:video/mp4;base64,AAAAHGZ0eXBNNFYgAAACAGlzb21pc28yYXZjMQAAAAhmcmVlAAA0Y21kYXQAAAKuBgX//6rcRem9
5tlIt5Ys2CDZI+7veDI2NCAtIGNvcmUgMTQ4IHIyNjQzIDVjNjU3MDQgLSBILjI2NC9NUEVHLTQg
QVZDIGNvZGVjIC0gQ29weWxlZnQgMjAwMy0yMDE1IC0gaHR0cDovL3d3dy52aWRlb2xhbi5vcmcv
eDI2NC5odG1sIC0gb3B0aW9uczogY2FiYWM9MSByZWY9MyBkZWJsb2NrPTE6MDowIGFuYWx5c2U9
MHgzOjB4MTEzIG1lPWhleCBzdWJtZT03IHBzeT0xIHBzeV9yZD0xLjAwOjAuMDAgbWl4ZWRfcmVm
PTEgbWVfcmFuZ2U9MTYgY2hyb21hX21lPTEgdHJlbGxpcz0xIDh4OGRjdD0xIGNxbT0wIGRlYWR6
b25lPTIxLDExIGZhc3RfcHNraXA9MSBjaHJvbWFfcXBfb2Zmc2V0PS0yIHRocmVhZHM9NiBsb29r
YWhlYWRfdGhyZWFkcz0xIHNsaWNlZF90aHJlYWRzPTAgbnI9MCBkZWNpbWF0ZT0xIGludGVybGFj
ZWQ9MCBibHVyYXlfY29tcGF0PTAgY29uc3RyYWluZWRfaW50cmE9MCBiZnJhbWVzPTMgYl9weXJh
bWlkPTIgYl9hZGFwdD0xIGJfYmlhcz0wIGRpcmVjdD0xIHdlaWdodGI9MSBvcGVuX2dvcD0wIHdl
aWdodHA9MiBrZXlpbnQ9MjUwIGtleWludF9taW49MjUgc2NlbmVjdXQ9NDAgaW50cmFfcmVmcmVz
aD0wIHJjX2xvb2thaGVhZD00MCByYz1jcmYgbWJ0cmVlPTEgY3JmPTIzLjAgcWNvbXA9MC42MCBx
cG1pbj0wIHFwbWF4PTY5IHFwc3RlcD00IGlwX3JhdGlvPTEuNDAgYXE9MToxLjAwAIAAAAjWZYiE
ADP//vbsvgU1/Z/QlxEsxdpKcD4qpICAdzTAAAADAAADAACG7EIUw97UeeSAAACuk6D+0h5/mARi
0XULsmlvpKot7Sz4frb8o2+zU/16U/z9F1Rb1AJWa68axPMz9HbCQ5fl+fnnxTDzaj+/4OO6bKuf
BlEweZ/w/VDAvias5Y421HQcLXLv2orVR/HfGLDgB/K6+wZY44AAS0XFjKuQ+4xFhJ5Z1YWIgmpj
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
AAAAAAAAAQAACWAAAAIAAAEAAAAAB3BtZGlhAAAAIG1kaGQAAAAAAAAAAAAAAAAAADIAAAB4AFXE
AAAAAAAtaGRscgAAAAAAAAAAdmlkZQAAAAAAAAAAAAAAAFZpZGVvSGFuZGxlcgAAAAcbbWluZgAA
ABR2bWhkAAAAAQAAAAAAAAAAAAAAJGRpbmYAAAAcZHJlZgAAAAAAAAABAAAADHVybCAAAAABAAAG
23N0YmwAAACzc3RzZAAAAAAAAAABAAAAo2F2YzEAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAACQAEg
AEgAAABIAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY//8AAAAxYXZj
QwFkAB7/4QAYZ2QAHqzZQJAloQAAAwABAAADAGQPFi2WAQAGaOvjyyLAAAAAHHV1aWRraEDyXyRP
xbo5pRvPAyPzAAAAAAAAABhzdHRzAAAAAAAAAAEAAAB4AAABAAAAABRzdHNzAAAAAAAAAAEAAAAB
AAAD0GN0dHMAAAAAAAAAeAAAAAEAAAIAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAA
AAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAA
AAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAA
AQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAAB
AAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEA
AAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAA
AQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAA
AAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIA
AAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAA
AAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAA
AAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAA
AQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAAB
AAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEA
AAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAA
BQAAAAABAAACAAAAAAEAAAAAAAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAAB
AAAAAAEAAAUAAAAAAQAAAgAAAAABAAAAAAAAAAEAAAEAAAAAAQAABQAAAAABAAACAAAAAAEAAAAA
AAAAAQAAAQAAAAABAAAFAAAAAAEAAAIAAAAAAQAAAAAAAAABAAABAAAAAAEAAAQAAAAAAQAAAgAA
AAABAAAAAAAAABxzdHNjAAAAAAAAAAEAAAABAAAAeAAAAAEAAAH0c3RzegAAAAAAAAAAAAAAeAAA
C4wAAAFYAAAAbQAAAFcAAABRAAABCgAAAFgAAABIAAAARgAAAPMAAABXAAAARwAAAD8AAADdAAAA
UQAAADMAAAA6AAABDAAAAEsAAAA4AAAAMwAAAOUAAABDAAAALwAAADIAAAD4AAAAUwAAAD4AAABC
AAAA5wAAAD8AAAA+AAAALwAAAPAAAAA9AAAANAAAADoAAACsAAAAPgAAADcAAAA4AAAApQAAADwA
AAA3AAAANgAAAMMAAAA/AAAANQAAADYAAACmAAAAPwAAADYAAAA3AAAAqgAAAEIAAAA0AAAAMwAA
ALsAAAA+AAAAMgAAADIAAAC4AAAAUgAAADYAAAA8AAAAhQAAAFcAAAA6AAAAOQAAAPQAAABeAAAA
RAAAADwAAACjAAAAQgAAAEMAAAAxAAAAfAAAADkAAAAvAAAALQAAAM4AAABAAAAALwAAAC0AAAB6
AAAAMwAAACkAAAAqAAAAoAAAADEAAAAmAAAAKAAAAG0AAAAwAAAAKAAAACkAAABlAAAAOAAAACkA
AAAkAAAAZgAAADMAAAAnAAAAJwAAAGQAAAA0AAAAKQAAACkAAABvAAAAQwAAACwAAAArAAAATQAA
AEwAAAA2AAAALAAAACwAAAAeAAAAJgAAABRzdGNvAAAAAAAAAAEAAAAsAAAAYnVkdGEAAABabWV0
YQAAAAAAAAAhaGRscgAAAAAAAAAAbWRpcmFwcGwAAAAAAAAAAAAAAAAtaWxzdAAAACWpdG9vAAAA
HWRhdGEAAAABAAAAAExhdmY1Ni40MC4xMDE=
">
  Your browser does not support the video tag.
</video>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Note that the second case has a much shallower potential well. This explains what IUPAC means when they say,</p>
<blockquote><p>depression on the potential energy surface that is deep enough to confine at least one vibrational state.</p>
</blockquote>
<p>In our second gif, the molecule's well is so shallow that the atoms just fall apart!</p>
<p>But in the first gif, the well is deeper and the atoms get trapped inside! We have a <strong>stable</strong> molecule, which is the question we tried to answer!</p>
</div>
</div>
</div>
<script type="text/javascript">if (!document.getElementById("mathjaxscript_pelican_#%@#$@#")) {
    var mathjaxscript = document.createElement("script");
    mathjaxscript.id = "mathjaxscript_pelican_#%@#$@#";
    mathjaxscript.type = "text/javascript";
    mathjaxscript.src = "//cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML";
    mathjaxscript[(window.opera ? "innerHTML" : "text")] =
        "MathJax.Hub.Config({" +
        "    config: ['MMLorHTML.js']," +
        "    TeX: { extensions: ['AMSmath.js', 'AMSsymbols.js', 'noErrors.js', 'noUndefined.js'], equationNumbers: { autoNumber: 'AMS' } }," +
        "    jax: ['input/TeX', 'input/MathML', 'output/HTML-CSS']," +
        "    extensions: ['tex2jax.js', 'mml2jax.js', 'MathMenu.js', 'MathZoom.js']," +
        "    displayAlign: 'center'," +
        "    displayIndent: '0em'," +
        "    showMathMenu: true," +
        "    tex2jax: { " +
        "        inlineMath: [ ['$', '$'] ], " +
        "        displayMath: [ ['$$', '$$'] ]," +
        "        processEscapes: true," +
        "        preview: 'TeX'," +
        "    }, " +
        "    'HTML-CSS': { " +
        " linebreaks: { automatic: true, width: '95% container' }, " +
        "        styles: { '.MathJax_Display, .MathJax .mo, .MathJax .mi, .MathJax .mn': {color: 'black ! important'} }" +
        "    } " +
        "}); ";
    (document.body || document.getElementsByTagName("head")[0]).appendChild(mathjaxscript);
}
</script>

</div>