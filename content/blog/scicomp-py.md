
---
author: Evan Curtin
date: 2016-10-26
slug: scientific-toolkit
tags:
- Python
- science
title: The Scientific computing toolkit for Python

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
<h2 id="Getting-Started">Getting Started<a class="anchor-link" href="#Getting-Started">&#182;</a></h2><hr>
<p>This presentation is no help if you can't get the python packages it uses! There are a few options here. If you're not already set up, probably the easiest way to install python packages is <a href="https://pip.pypa.io/en/stable/">pip</a>. If you don't already have it, here are <a href="https://packaging.python.org/installing/#install-pip-setuptools-and-wheel">installation instructions</a>. I'm a big fan of the <a href="https://www.continuum.io/">anaconda</a> python distrubution, which comes pre-loaded with basically everything I'm using today. Just use whatever works for you.</p>
<p>For example, installing numpy is easy, in a command line:</p>
<p>pip install numpy</p>
<p>If you're using anaconda, you can also use their package manager:</p>
<p>conda install numpy</p>
<p>Pip is probably the preferred method, even when you're using anaconda. The packages I'm discussing today are <a href="http://www.numpy.org/">numpy</a>, <a href="https://www.scipy.org/">scipy</a>, <a href="http://pandas.pydata.org/">pandas</a>, <a href="http://matplotlib.org/">matplotlib</a>, <a href="https://seaborn.github.io/">seaborn</a>.</p>
<p>Other useful tools are <a href="http://numba.pydata.org/">Numba</a> and <a href="http://cython.org/">Cython</a>. As far as I know, all of these are in both package managers.</p>
<p>I've recently been told that pandas depends on cython and seaborn depends on pandas.</p>
<p>You should therefore install cython -&gt; pandas -&gt; seaborn in that order.</p>
<p>This talk was made using a <a href="http://jupyter.org/">jupyter</a> notebook.</p>
<h2 id="Python-is-slow!-Why-bother?">Python is slow! Why bother?<a class="anchor-link" href="#Python-is-slow!-Why-bother?">&#182;</a></h2><hr>
<p>This is a common reason people want to avoid python, and it's half true. See for example this function that performs a matrix multiplication:</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">import</span> <span class="nn">math</span>
<span class="n">N</span> <span class="o">=</span> <span class="mi">300</span>
<span class="n">mat1</span> <span class="o">=</span> <span class="p">[[</span><span class="mf">1.5</span><span class="o">*</span><span class="n">i</span> <span class="o">+</span> <span class="n">j</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">)]</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">)]</span>
<span class="n">mat2</span> <span class="o">=</span> <span class="p">[[</span><span class="mf">2.5</span><span class="o">*</span><span class="n">i</span> <span class="o">+</span> <span class="n">j</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">)]</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">)]</span>
<span class="k">def</span> <span class="nf">mmult</span><span class="p">(</span><span class="n">mat1</span><span class="p">,</span> <span class="n">mat2</span><span class="p">):</span>
    <span class="n">mat3</span> <span class="o">=</span> <span class="p">[[</span><span class="mf">0.0</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">)]</span> <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">)]</span>
    <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">):</span>
        <span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">):</span>
            <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">):</span>
                <span class="n">mat3</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">]</span> <span class="o">+=</span> <span class="n">mat1</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">]</span> <span class="o">*</span> <span class="n">mat2</span><span class="p">[</span><span class="n">j</span><span class="p">][</span><span class="n">k</span><span class="p">]</span>
    <span class="k">return</span> <span class="n">mat3</span>
<span class="o">%</span><span class="n">time</span> <span class="n">m3</span> <span class="o">=</span> <span class="n">mmult</span><span class="p">(</span><span class="n">mat1</span><span class="p">,</span> <span class="n">mat2</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>CPU times: user 3.78 s, sys: 0 ns, total: 3.78 s
Wall time: 3.78 s
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Well that doesn't seem so bad! This would take longer to do by hand! It actually is pretty slow.  <a href="https://jakevdp.github.io/blog/2014/05/09/why-python-is-slow/">Here's</a>
a look at some of the reasons why. It has to do with the fact that python is dynamically typed and interpreted, rather than compiled. Additionally, the arrays in native python aren't laid out in one chunk of memory.</p>
<h2 id="It-doesn't-have-to-be-this-way!-(Numpy-section)">It doesn't have to be this way! (Numpy section)<a class="anchor-link" href="#It-doesn't-have-to-be-this-way!-(Numpy-section)">&#182;</a></h2><hr>
<p>If you're going to be doing serious numerical work in python, numpy is essential. If you're doing a lot of work with arrays, the performance difference between raw python and C/C++/Fortran can easily be several orders of magnitude. Numpy is focused on fast, efficient manipulation of arrays. They can be any size, any dimension as long as your computer can store it. Numpy methods are compiled and very efficient (comparable to compiled code). Let's take a look at our matrix multiply again:</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="kn">as</span> <span class="nn">np</span> <span class="c1"># convention</span>
<span class="n">npmat1</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">asarray</span><span class="p">(</span><span class="n">mat1</span><span class="p">)</span> <span class="c1"># use numpy arrays, they are contiguous in memory</span>
<span class="n">npmat2</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">asarray</span><span class="p">(</span><span class="n">mat2</span><span class="p">)</span>
<span class="o">%</span><span class="n">time</span> <span class="n">npmat3</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">dot</span><span class="p">(</span><span class="n">npmat1</span><span class="p">,</span> <span class="n">npmat2</span><span class="p">)</span> <span class="c1"># dot is used for dot product or matrix multiply</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>CPU times: user 4 ms, sys: 4 ms, total: 8 ms
Wall time: 5.86 ms
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>WHOA! Blazing fast! Morale of the story: if there is a numpy function to do it, use it! And there  is a numpy function for a lot of stuff, here's a few useful ones:</p>
<p><a href="http://docs.scipy.org/doc/numpy-1.10.0/reference/generated/numpy.linalg.eig.html">np.linalg.eig</a> - eigenvectors/values</p>
<p><a href="http://docs.scipy.org/doc/numpy/reference/generated/numpy.zeros.html">np.zeros</a> - create an array of zeros</p>
<p><a href="http://docs.scipy.org/doc/numpy/reference/generated/numpy.linspace.html">np.linspace</a> - create an array of values spaced linearly between 2 endpoints</p>
<p><a href="http://docs.scipy.org/doc/numpy-1.10.1/reference/generated/numpy.sort.html">np.sort</a> - Sort an array</p>
<p><a href="http://docs.scipy.org/doc/numpy/reference/generated/numpy.amax.html">np.amax</a> - Return maximum value of array</p>
<p><a href="http://docs.scipy.org/doc/numpy/reference/generated/numpy.random.rand.html">np.random.rand</a> - create array of random values in [0, 1)</p>
<p>There's about 3 trillion more ...</p>
<h2 id="A-few-useful-tips-about-numpy-arrays:">A few useful tips about numpy arrays:<a class="anchor-link" href="#A-few-useful-tips-about-numpy-arrays:">&#182;</a></h2><hr>
<h3 id="1)-Most-'normal'-operations-are-element-wise:">1) Most 'normal' operations are element-wise:<a class="anchor-link" href="#1)-Most-'normal'-operations-are-element-wise:">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">A</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>
             <span class="p">,[</span><span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">]</span>
             <span class="p">,[</span><span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">9</span><span class="p">]])</span>
<span class="k">print</span><span class="p">(</span><span class="mi">10</span> <span class="o">+</span> <span class="n">A</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[11 12 13]
 [14 15 16]
 [17 18 19]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">print</span><span class="p">(</span><span class="mi">2</span> <span class="o">*</span> <span class="n">A</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[ 2  4  6]
 [ 8 10 12]
 [14 16 18]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">print</span><span class="p">(</span><span class="n">A</span> <span class="o">==</span> <span class="mi">5</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[False False False]
 [False  True False]
 [False False False]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">B</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mi">10</span><span class="p">,</span> <span class="mi">20</span><span class="p">,</span> <span class="mi">30</span><span class="p">]</span>
             <span class="p">,[</span><span class="mi">40</span><span class="p">,</span> <span class="mi">50</span><span class="p">,</span> <span class="mi">60</span><span class="p">]</span>
             <span class="p">,[</span><span class="mi">70</span><span class="p">,</span> <span class="mi">80</span><span class="p">,</span> <span class="mi">90</span><span class="p">]])</span>
<span class="k">print</span><span class="p">(</span><span class="n">A</span> <span class="o">+</span> <span class="n">B</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[11 22 33]
 [44 55 66]
 [77 88 99]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="2)-You-can-'slice'-numpy-arrays">2) You can 'slice' numpy arrays<a class="anchor-link" href="#2)-You-can-'slice'-numpy-arrays">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">,</span> <span class="s1">&#39;</span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">)</span>
<span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">[:,</span> <span class="mi">2</span><span class="p">])</span>  <span class="c1"># 3rd column (starts at 0)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[1 2 3]
 [4 5 6]
 [7 8 9]]
[3 6 9]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="p">:])</span>  <span class="c1">#Second row</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[4 5 6]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="mi">2</span><span class="p">,</span> <span class="mi">0</span><span class="p">:</span><span class="mi">2</span><span class="p">])</span> <span class="c1"># Top-Left 2x2 section</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[1 2]
 [4 5]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="3)-You-can-index-a-numpy-array...-with-a-numpy-array">3) You can index a numpy array... with a numpy array<a class="anchor-link" href="#3)-You-can-index-a-numpy-array...-with-a-numpy-array">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">indices</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="p">])</span>
<span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[1 2 3]
 [4 5 6]
 [7 8 9]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">[</span><span class="n">indices</span><span class="p">])</span>  <span class="c1"># first and third row</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[1 2 3]
 [7 8 9]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">[:,</span><span class="n">indices</span><span class="p">])</span>  <span class="c1"># first and third column</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[1 3]
 [4 6]
 [7 9]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">indices2</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">asarray</span><span class="p">([[</span><span class="bp">True</span><span class="p">,</span> <span class="bp">True</span><span class="p">,</span> <span class="bp">False</span><span class="p">]</span>
                     <span class="p">,[</span><span class="bp">False</span><span class="p">,</span> <span class="bp">True</span><span class="p">,</span> <span class="bp">True</span><span class="p">]</span>
                     <span class="p">,[</span><span class="bp">False</span><span class="p">,</span> <span class="bp">False</span><span class="p">,</span> <span class="bp">False</span><span class="p">]])</span>
<span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">,</span> <span class="s1">&#39;</span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">)</span>
<span class="k">print</span><span class="p">(</span><span class="n">A</span><span class="p">[</span><span class="n">indices2</span><span class="p">])</span>  <span class="c1"># All elements where indices2 is True</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[[1 2 3]
 [4 5 6]
 [7 8 9]]
[1 2 5 6]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="4)-And-you-can-combine-operations">4) And you can combine operations<a class="anchor-link" href="#4)-And-you-can-combine-operations">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">symmetric</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
                     <span class="p">,[</span><span class="mi">4</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
                     <span class="p">,[</span><span class="mi">4</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">1</span><span class="p">]])</span>
<span class="n">asymmetric</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
                      <span class="p">,[</span><span class="mi">7</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
                      <span class="p">,[</span><span class="mi">42</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">1</span><span class="p">]])</span>
</pre></div>
    </div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Maybe to check if a matrix is symmetric</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">all</span><span class="p">(</span><span class="n">symmetric</span><span class="o">.</span><span class="n">T</span> <span class="o">==</span> <span class="n">symmetric</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[15]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>True</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">all</span><span class="p">(</span><span class="n">asymmetric</span><span class="o">.</span><span class="n">T</span> <span class="o">==</span> <span class="n">asymmetric</span><span class="p">)</span>  <span class="c1"># WARNING if using floats, compare</span>
                                    <span class="c1"># with np.isclose(x.T, x)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[16]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>False</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Or to sort eigenvales and eigenvectors so that the eigenvalues are in ascending order, and you keep track of the vectors!</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">vals</span><span class="p">,</span> <span class="n">vecs</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linalg</span><span class="o">.</span><span class="n">eig</span><span class="p">(</span><span class="n">symmetric</span><span class="p">)</span>
<span class="k">print</span><span class="p">(</span><span class="n">vals</span><span class="p">)</span>
<span class="k">print</span><span class="p">(</span><span class="n">vecs</span><span class="p">)</span>
<span class="k">print</span><span class="p">(</span><span class="s1">&#39;</span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">)</span>
<span class="n">indices_of_sorted_vals</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">argsort</span><span class="p">(</span><span class="n">vals</span><span class="p">)</span>
<span class="k">print</span><span class="p">(</span><span class="n">vals</span><span class="p">[</span><span class="n">indices_of_sorted_vals</span><span class="p">])</span>
<span class="k">print</span><span class="p">(</span><span class="n">vecs</span><span class="p">[:,</span> <span class="n">indices_of_sorted_vals</span><span class="p">])</span>  <span class="c1"># columns are rearranged</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>[-3.  9. -3.]
[[-0.81649658  0.57735027  0.19219669]
 [ 0.40824829  0.57735027 -0.7833358 ]
 [ 0.40824829  0.57735027  0.59113912]]
[-3. -3.  9.]
[[-0.81649658  0.19219669  0.57735027]
 [ 0.40824829 -0.7833358   0.57735027]
 [ 0.40824829  0.59113912  0.57735027]]
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Scipy">Scipy<a class="anchor-link" href="#Scipy">&#182;</a></h2><hr>
<p>We're all scientists here, so It would be silly to avoid scipy. It's a library of scientifically relevant tools. Here's a list of some of the submodules:</p>
<p>Special functions (scipy.special)</p>
<p>Integration (scipy.integrate)</p>
<p>Optimization (scipy.optimize)</p>
<p>Interpolation (scipy.interpolate)</p>
<p>Fourier Transforms (scipy.fftpack)</p>
<p>Signal Processing (scipy.signal)</p>
<p>Linear Algebra (scipy.linalg)</p>
<p>Sparse Eigenvalue Problems with ARPACK</p>
<p>Compressed Sparse Graph Routines (scipy.sparse.csgraph)</p>
<p>Spatial data structures and algorithms (scipy.spatial)</p>
<p>Statistics (scipy.stats)</p>
<p>Multidimensional image processing (scipy.ndimage)</p>
<p>File IO (scipy.io)</p>
<p>Weave (scipy.weave)</p>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The various python modules make it super easy to do lots of things, like making a function that returns the nth harmonic oscillator wavefunction:</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">from</span> <span class="nn">math</span> <span class="kn">import</span> <span class="n">factorial</span><span class="p">,</span> <span class="n">pi</span>
<span class="kn">from</span> <span class="nn">scipy.special</span> <span class="kn">import</span> <span class="n">hermite</span> <span class="k">as</span> <span class="n">h</span>
<span class="k">def</span> <span class="nf">psi</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">n</span><span class="p">):</span>
    <span class="n">N</span> <span class="o">=</span> <span class="mf">1.0</span> <span class="o">/</span> <span class="n">np</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="mi">2</span><span class="o">**</span><span class="n">n</span><span class="p">)</span> <span class="o">*</span> <span class="n">factorial</span><span class="p">(</span><span class="n">n</span><span class="p">))</span> <span class="o">*</span> <span class="p">(</span><span class="mf">1.0</span> <span class="o">/</span> <span class="n">pi</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">N</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="o">-</span><span class="n">x</span><span class="o">*</span><span class="n">x</span> <span class="o">/</span> <span class="mf">2.0</span><span class="p">)</span> <span class="o">*</span> <span class="n">h</span><span class="p">(</span><span class="n">n</span><span class="p">)(</span><span class="n">x</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>If I try to cover all of scipy it will get boring fast... you can look up functions as you need them</p>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Matplotlib">Matplotlib<a class="anchor-link" href="#Matplotlib">&#182;</a></h2><hr>
<p>Matplotlib is the tool to go to for quick plotting stuff in Python. It can handle 2D, 3D, and even animations.</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="kn">as</span> <span class="nn">plt</span>
<span class="c1"># Jupyter  &quot;Magic&quot;, just so you see the images in the notebook</span>
<span class="o">%</span><span class="n">matplotlib</span> <span class="n">inline</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">6</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">100</span><span class="p">)</span>   <span class="c1"># list of x from 0 to 10 by 100 steps</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>                 <span class="c1"># take the sign of each element in x</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>                <span class="c1"># do I have to explain this one?</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
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
<p>To plot multiple things at once, call plt.plot() more than once</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="k">def</span> <span class="nf">plot_HO</span><span class="p">(</span><span class="n">N</span><span class="p">):</span> <span class="c1"># plot N wavefunctions</span>
    <span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">6</span><span class="p">,</span><span class="mi">6</span><span class="p">))</span>
    <span class="n">ymax</span> <span class="o">=</span> <span class="n">N</span> <span class="o">+</span> <span class="mf">1.5</span>
    <span class="n">xmax</span> <span class="o">=</span> <span class="n">math</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">ymax</span><span class="p">)</span>    <span class="c1"># figuring out plot ranges</span>
    <span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="o">-</span><span class="n">xmax</span><span class="p">,</span> <span class="n">xmax</span><span class="p">,</span> <span class="mi">100</span><span class="p">)</span>
    <span class="k">for</span> <span class="n">n</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">N</span><span class="p">):</span>                       <span class="c1"># from n = [0...N)</span>
        <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">psi</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">n</span><span class="p">)</span> <span class="o">+</span> <span class="p">(</span><span class="n">n</span> <span class="o">+</span> <span class="mf">0.5</span><span class="p">))</span>   <span class="c1"># Plot the wavefunction offset by</span>
                                             <span class="c1"># energy</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="mf">0.5</span> <span class="o">*</span> <span class="n">x</span><span class="o">*</span><span class="n">x</span><span class="p">,</span> <span class="s1">&#39;k&#39;</span><span class="p">)</span>  <span class="c1"># Plot the potential</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlim</span><span class="p">(</span><span class="o">-</span><span class="n">xmax</span><span class="p">,</span> <span class="n">xmax</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylim</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="n">ymax</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
<span class="n">plot_HO</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_png output_subarea ">
<img src="data:image/png;base64,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wycdgJSSdevWccMNN/Dyyy8zf/588vLyuP/++9VYdhBRiVu5osTERP7+97+zZ88eYmJimDlzJunp6Rw6dEjv0ILWF198wZgxY5g3bx5JSUns37+ft99+m/j4eL1DU9qZStzKf3Tbbbfx9ddfs3LlSnJzc0lLS2PevHkUFhbqHVrQyM/PZ+bMmYwePZrTp0+zZs0a9u/fz6hRo/QOTdGJStzKVRmNRh577DHy8/N56qmn2LRpEwMHDuSJJ56gtLRU7/ACVnFxMY888giDBg3in//8J8899xynTp3ioYceUicfg11Li5pcy00VmQpsRUVFcuHChdJgMEir1SqXLl0qz507p3dYAaOkpEQuXrxYms1maTKZ5OOPP66KQgUBVJEppS316tWL1atXc+LECWbNmsWf/vQn+vTpw+OPP05BQYHe4XVap06dYtGiRaSkpLBq1SoWLFhAfn4+f/3rX1VRKKUZlbiV69avXz/effddjh8/zrx581i9ejX9+/dn7ty5HDhwQO/wOgUpJZ999hmzZs0iNTWV999/n0WLFnHy5EnefPNNkpOT9Q5R6YBU4lZ+toEDB7J69WpOnz7NkiVL+Pjjj7npppsYPXo069evx+Vy6R1ih+NwOFi7di0jR45kzJgx5OTksGzZMgoKCli5ciUpKSl6h6h0YCpxK62mZ8+evPrqq5SUlPDaa69RXl7OnDlz6NmzJ7/73e/Iy8vTO0TdffvttyxZsoQePXpw//33Y7PZeP311ykpKeHFF1+kW7dueoeodAK6LxasBC6fz8fOnTtZvXo127Ztw+PxcMstt3Dfffdx7733kpCQoHeI7eLcuXOsX7+edevWcfDgQcxmM9OnT2fhwoXcdddd6sIZBegAiwWrxK382Pnz53n33Xd5//33yc3NxWAwkJGRwbRp05g6dWrA9TTPnDnDRx99xObNm9m9ezc+n4/hw4czb9485s+fry6aUS6jErfSoeXm5rJu3To2bNjADz/8gBCCW265hUmTJpGZmcnw4cM73Txlr9fLgQMHyM7OZseOHXz11VeANv4/a9Ys5s6dS2pqqs5RKh1ZqyduIcQE4DXAAKyRUv7xPz1eJW6lJaSU5ObmsnXrVrZu3crhw4cBiIuL484772Ts2LGMHTuWoUOHdrjltjweD0eOHGHfvn3s27eP3bt3U11djRCCESNGcM899zBt2jRSU1PVUIjSIq2auIUQBuAkkAGUAAeAOVLKn1xtViVu5XqUlZWRk5NDdnY2e/bsoaioCICIiAiGDRvG8OHDSUtLY8iQIQwcOJDw8PB2iau+vp4TJ06Qm5vLoUOHOHToEIcPH26qmti3b19uv/12MjMzSU9PV8MgynVp7cR9C/CslDLT//VTAFLKF3/qOSpxK62hqKiITz/9lC+++IKvv/6aI0eOYLfbm37eu3dvBgwYQHJyctOta9euxMfHEx8fT3R0NGFhYVit1suGXnw+Hw6HA5vNRnV1NRUVFVRUVHD+/HmKi4spKiqisLCQU6dOUVxc3PS88PBwhg0bRlpaGqNHj+bWW2+lZ8+e7bZNlMDV2ol7JjBBSrnQ//V8YJSUcvFPPUclbqUteL1eTpw4wXfffUdeXh55eXnk5+dTVFR01ZopFoulachCSonT6fzJxwoh6N69O8nJyQwYMIDU1FRSU1MZPHgwAwYM6HDDNkpguJbEbWzJ613he5dleyHEw8DD/i/rhRAnWhJAO4kHKvQOQmdBvQ0uSdRX3Q5SSs6ePcvZs2fZv39/m8emk6B+P/h1tG3Qu6UPbEniLgF6XfJ1EnD2xw+SUr4JvNnSX9yehBAHW7onC1RqG2jUdtCo7dC5t0FL5lwdAAYIIVKEEGZgNrCtbcNSFEVRfspVe9xSSo8QYjGQjTYd8G0p5bE2j0xRFEW5opYMlSCl3AHsaONY2lKHHMJpZ2obaNR20Kjt0Im3QZtcOakoiqK0nc51XbGiKIoSHIlbCPGyECJPCHFUCLFFCBGjd0x6EEL8SghxTAjhE0J0yrPp10sIMUEIcUIIkS+EWK53PHoRQrwthCgTQnyrdyx6EUL0EkLsFkIc938elugd07UKisQN5ABDpJRD0S7ff0rnePTyLTAd2Kt3IO3JX7ZhJTARGAzMEUIM1jcq3bwDTNA7CJ15gN9KKQcBNwOPd7b3Q1AkbinlTimlx//lfrS56EFHSnlcStmRLoxqLzcB+VLKH6SULmA9MFXnmHQhpdwLXNA7Dj1JKUullIf89+uA40CnqlsQFIn7Rx4EPtE7CKVd9QSKL/m6hE72QVXahhCiDzAM+FLfSK5Ni6YDdgZCiF3AlZbC/m8p5Uf+x/w32mHSuvaMrT21ZDsEoRaVbVCCixAiAtgE/EZKWat3PNciYBK3lHLcf/q5EGIBMBlIlwE8B/Jq2yFItahsgxI8hBAmtKS9Tkq5We94rlVQDJX4F4L4PTBFSmnTOx6l3amyDUoToZWJfAs4LqX8f3rHcz2CInEDfwUigRwhxBEhxCq9A9KDEGKaEKIEuAXIEkJk6x1Te/CfmG4s23Ac+Eewlm0QQnwAfAHcIIQoEUI8pHdMOrgVmA/c5c8HR4QQk/QO6lqoKycVRVE6mWDpcSuKogQMlbgVRVE6GZW4FUVROhmVuBVFUToZlbgVRVE6GZW4FUVROhmVuBVFUToZlbgVRVE6mf8DXrJJE4d4wTcAAAAASUVORK5CYII=
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
<p>Matplotlib has functions for scatterplots, pie charts, bar graphs, heatmaps blah blah blah...</p>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Pandas">Pandas<a class="anchor-link" href="#Pandas">&#182;</a></h2><hr>
<p>I recently started using Pandas in my research, and It's already proven incredibly useful for data analysis. The library is focused on the Series and the DataFrame.</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="kn">as</span> <span class="nn">pd</span>
<span class="n">series1</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">Series</span><span class="p">([</span><span class="mi">4</span><span class="p">,</span> <span class="mf">2.5</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">72</span><span class="p">])</span>
<span class="n">series1</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[21]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>0     4.0
1     2.5
2     8.0
3    72.0
dtype: float64</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>I don't know about you, but this isn't the most impressive thing to me... just hold on.</p>
<p>Here's an example of a DataFrame, the reason I'm in love with this library</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">Cols</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Rain&#39;</span><span class="p">,</span> <span class="s1">&#39;Temperature&#39;</span><span class="p">,</span> <span class="s1">&#39;Wind&#39;</span><span class="p">]</span>
<span class="n">Dates</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">date_range</span><span class="p">(</span><span class="s1">&#39;20161020&#39;</span><span class="p">,</span> <span class="n">periods</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
<span class="n">data</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">3</span><span class="p">)</span> <span class="c1"># 3 cols 10 rows</span>
<span class="n">df</span><span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">index</span><span class="o">=</span><span class="n">Dates</span><span class="p">,</span> <span class="n">columns</span><span class="o">=</span><span class="n">Cols</span><span class="p">)</span>
<span class="n">df</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[22]:</div>
<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }
    .dataframe tbody tr th {
        vertical-align: top;
    }
    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rain</th>
      <th>Temperature</th>
      <th>Wind</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2016-10-20</th>
      <td>0.193955</td>
      <td>0.350702</td>
      <td>0.618494</td>
    </tr>
    <tr>
      <th>2016-10-21</th>
      <td>0.707791</td>
      <td>0.823698</td>
      <td>0.548552</td>
    </tr>
    <tr>
      <th>2016-10-22</th>
      <td>0.851024</td>
      <td>0.983293</td>
      <td>0.709565</td>
    </tr>
    <tr>
      <th>2016-10-23</th>
      <td>0.434959</td>
      <td>0.669047</td>
      <td>0.405353</td>
    </tr>
    <tr>
      <th>2016-10-24</th>
      <td>0.398242</td>
      <td>0.252898</td>
      <td>0.604027</td>
    </tr>
    <tr>
      <th>2016-10-25</th>
      <td>0.620698</td>
      <td>0.142928</td>
      <td>0.551496</td>
    </tr>
    <tr>
      <th>2016-10-26</th>
      <td>0.438231</td>
      <td>0.620494</td>
      <td>0.525627</td>
    </tr>
    <tr>
      <th>2016-10-27</th>
      <td>0.424516</td>
      <td>0.189178</td>
      <td>0.570212</td>
    </tr>
    <tr>
      <th>2016-10-28</th>
      <td>0.093206</td>
      <td>0.278414</td>
      <td>0.980758</td>
    </tr>
    <tr>
      <th>2016-10-29</th>
      <td>0.429858</td>
      <td>0.857150</td>
      <td>0.886912</td>
    </tr>
  </tbody>
</table>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Rain&#39;</span><span class="p">]</span>  <span class="c1"># Grab all the stuff in &#39;Rain&#39; column</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[23]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>2016-10-20    0.193955
2016-10-21    0.707791
2016-10-22    0.851024
2016-10-23    0.434959
2016-10-24    0.398242
2016-10-25    0.620698
2016-10-26    0.438231
2016-10-27    0.424516
2016-10-28    0.093206
2016-10-29    0.429858
Freq: D, Name: Rain, dtype: float64</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="s1">&#39;2016-10-23&#39;</span><span class="p">]</span>  <span class="c1"># locate this date</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[24]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>Rain           0.434959
Temperature    0.669047
Wind           0.405353
Name: 2016-10-23 00:00:00, dtype: float64</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">iloc</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span>  <span class="c1"># grab the 3rd row</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[25]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>Rain           0.851024
Temperature    0.983293
Wind           0.709565
Name: 2016-10-22 00:00:00, dtype: float64</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[26]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">plot</span><span class="p">()</span>  <span class="c1"># Plot all the stuff</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[26]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7f67de0d2e80&gt;</pre>
</div>
</div>
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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">plot</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;Rain&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;Temperature&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlim</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
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
<p>You can find data by name and apply an operation to it, like checking which days had small amounts of rain:</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Rain&#39;</span><span class="p">]</span> <span class="o">&lt;</span> <span class="mf">0.1</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[28]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>2016-10-20    False
2016-10-21    False
2016-10-22    False
2016-10-23    False
2016-10-24    False
2016-10-25    False
2016-10-26    False
2016-10-27    False
2016-10-28     True
2016-10-29    False
Freq: D, Name: Rain, dtype: bool</pre>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Hmm, that's pretty nice isn't it? What if we could easily select only the parts that satisfy our condition? ....</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[29]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Rain&#39;</span><span class="p">]</span> <span class="o">&lt;</span> <span class="mf">0.1</span><span class="p">]</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[29]:</div>
<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }
    .dataframe tbody tr th {
        vertical-align: top;
    }
    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rain</th>
      <th>Temperature</th>
      <th>Wind</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2016-10-28</th>
      <td>0.093206</td>
      <td>0.278414</td>
      <td>0.980758</td>
    </tr>
  </tbody>
</table>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Ok that's pretty neat. I think this alone is useful. But we're just getting started!</p>
<p>What if we could find all parts of our data frame that satisfy a given condition, then plot two other columns of that data? Say no more...</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[30]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">TempsAbove</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;Temperature&#39;</span><span class="p">]</span> <span class="o">&gt;</span> <span class="mf">0.5</span><span class="p">]</span>
<span class="n">TempsAbove</span><span class="o">.</span><span class="n">plot</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="s1">&#39;Rain&#39;</span><span class="p">,</span> <span class="s1">&#39;Wind&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
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
<p>The reason I like this library so much is that you can use the past few examples, combining them as you wish, and analyze huge amounts of data in seconds. Lately I've written a function to do a custom plot on each row of a dataframe (optionally you can apply a condition to a dataframe and pass that through). I take my output files, parse them and put them into a dataframe. This lets me go from a directory of output files to a ton of plots in seconds, with little effort.</p>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Seaborn">Seaborn<a class="anchor-link" href="#Seaborn">&#182;</a></h2><hr>
<p><em>Update: As of matplotlib 2.0, the style defaults there are actually good. Seaborn is now less useful if you're not doing statistical plots. </em></p>
<p>Let's face it: I've been to enough talks to know that most people don't know how to make visually appealing figures. Well the good news is that you don't have to. Trust in Seaborn, for it is magnificent.</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[31]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="kn">import</span> <span class="nn">seaborn</span> <span class="kn">as</span> <span class="nn">sns</span> <span class="c1"># importing changes defaults</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylim</span><span class="p">(</span><span class="o">-</span><span class="mf">1.1</span><span class="p">,</span> <span class="mf">1.1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[31]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x7f67ddf5d3c8&gt;]</pre>
</div>
</div>
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
<p>This is the default with nothing done, the library was made to have nice colorschemes out of the box, but I prefer a less intrusive background</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[32]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">set_style</span><span class="p">(</span><span class="s1">&#39;white&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylim</span><span class="p">(</span><span class="o">-</span><span class="mf">1.1</span><span class="p">,</span> <span class="mf">1.1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[32]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x7f67dafe6cf8&gt;]</pre>
</div>
</div>
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
<p>Remember our harmonic oscillator plots?</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[33]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">plot_HO</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAWcAAAFiCAYAAAAqdRk+AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMS4yLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvNQv5yAAAIABJREFUeJzs3Xd8W9X9//GXpiVZlvfeI06cPcleBEIGgVACoeVbKKWDXwuUAiUFyiqFFgj0UQppS+mgA0pZCSMpkD0hg0w7TuLEjke8h2TJ1tbvj5s4bDuJbcn25/l46CGwr64+cqS3zj333HNUgUAggBBCiJCiDnYBQgghvkjCWQghQpCEsxBChCAJZyGECEESzkIIEYK0F7oDp9PJoUOHiI+PR6PRdEdNQgjR7/l8Purr6xk+fDgGg+ELv7/gcD506BDXX3/9he5GCCEGpH//+9+MHz/+Cz+/4HCOj4/veIKkpKQL3Z0QQgwINTU1XH/99R0Z+nkXHM5nujKSkpJIS0u70N0JIcSA8lXdwXJCUAghQpCEsxBChCAJZyGECEESzkIIEYIknIUQIgRJOAshRAiScBZCiBAk4SyEECFIwlkIIUKQhLMQQoQgCWchhAhBEs5CCBGCJJyFECIESTgLIUQIknAWQogQJOEshBAhSMJZCCFCkISzEEKEoC6Fs81m4/bbb2fevHnMnz+fvXv39nRdQggxoHVpDcHHHnuM6dOn8+yzz+J2u3E6nT1dlxBCDGidtpztdju7du1iyZIlAOj1eiwWS48XJoQQA1mn4VxRUUFMTAz33nsvixcv5v7776etra03ahNCiAGr03D2er0UFRXxzW9+k5UrV2I0GnnhhRd6ozYhhBiwOg3npKQkkpKSGDVqFADz5s2jqKioxwsTQoiBrNNwjo+PJykpiRMnTgCwY8cOcnNze7wwIYQYyLo0WuOBBx7g7rvvxuPxkJ6ezq9//euerksIIQa0LoVzQUEBb775Zk/XIoQQ4jS5QlAIIUKQhLMQQoQgCWchhAhBEs5CCBGCJJyFECIESTgLIUQIknAWQogQJOEshBAhSMJZCCFCkISzEEKEIAlnIYQIQRLOQggRgiSchRAiBEk4CyFECJJwFkKIECThLIQQIUjCWQghQpCEsxBChCAJZyGECEESzkIIEYIknIUQIgRJOAshRAiScBZCiBAk4SyEECFIwlkIIUKQhLMQQoQgCWchhAhBEs5CCBGCJJyFECIESTgLIUQIknAWQogQJOEshBAhSMJZCCFCkISzEEKEIAlnIYQIQRLOQggRgiSchRAiBEk4CyFECJJwFkKIECThLIQQIUjCWQghQpC2KxtdfPHFhIeHo1ar0Wg0vPnmmz1dlxBCDGhdCmeAl156iZiYmJ6sRQghxGnSrSGEECGoy+F88803841vfINXX321J+sRQghBF7s1XnnlFRITE2lsbOSmm24iJyeHCRMm9HRtQggxYHWp5ZyYmAhAbGwsl156KQcOHOjRooQQYqDrNJzb2tqw2+0d/71t2zYGDRrU44UJIcRA1mm3RmNjIz/+8Y8B8Pl8XH755cyYMaPHCxNCiIGs03BOT0/n7bff7o1ahBBCnCZD6YQQIgRJOAshRAiScBZCiBAk4SyEECFIwlkIIUKQhLMQQoQgCWchhAhBXZ4ytDP1Fa34rY24nT58Hh9ejx+fN0DAH/jMdhqdGq1OjUanRm/QEmZSboZwHYZwHSq1qrtKEkKIbhfwB2i3e3A6PLjbvbjavLjbvaczz4/P4//M9iq1Ssk8rQqNToPeoEFv1GJtaf/a5+m2cP7fHw9hMcZe0D7UGhUmi57wqDAssQYscUYs8UaiE03EpIQTZtJ1U7VCCPHVnA4PTacctNS2Ya1vx9ag3BxWN+02N/7PNTrPh6298Wt/323hfPGNBWRkpqM3aM62jrXqjpawSgUBP8o3i9eP1+3H7VS+dVxtHtrtHtqsbtqsLuwtLmpPtnL8k/rP/BHM0WHEppqJz4wgMdNCQpYFk0XfXS9B9COBwBc/PCqVHJWJL3JYXdSW2qgvb6XupI3GSjsOq7vj92q1iohYA5Z4IzGpZqUBGanHYNYRZtIRZtSiN2jR6pUeAY1WreTd6bdgwB9QMs+jtKrd7V7cTh8VFRX8/aOvrqvbwjk1P4rktMju2h0Afp+f1iYXzTUOmk45aDxlp6HCTnlhY8cLj0wwkjIoipS8KFIHRxMRY+jWGkRo8rh8NFTaaa52dLRsWpucOB0eXA4vrnbvZ7rUVGrVp7rPtETEnD0yi0kOJy7NjFavCeIrEr3F1tBO5ZFmqo+1cKqkBVuDE1DeIzEp4aQXxBCdEk5sipnoJBPmGAPqHuhu1UT1UrdGT1Br1ETGG4mMN5I1Iq7j526nl4YKO7WlNk6VtHBibz2Ht1UDEJ1kIn1oDBnDYknLj0ajk3Oe/UFrk5OqI81UHW2m7mQrzdWOji/oMy2biFgDlliD0poxaVFrz/7b+7x+3G1enG0enHYPtWU2Sj6p7whwlVpFTLKJhEwLqYOjSc2PxhwdFoyXKrqZ1+2j8kgz5YVNlBc1Yq1TQtEQriNlUBQjZqWRmB1JXLoZXQh9QYd0OH8VvUGrtJYHRTFmbgYBf4DGUw4qi5soL2qicPMpDqyvRBemIWNYDNmj4skaGUeYsU++3AHJ5/NTfayFE/sbKD/UiLX+7AcqMcdCzph4EjIiiE01Y44OQ6059y9h5cjMSWOlg7py5bD2xL56Dm9XvuijEk1kDo8lZ3QcSblRPdJ6Ej3D6fBQdqCBE/vqqTjchNftR6tTk5IfzYiZaaQVRBOTHB7SXV39Iq1UahVxaWbi0syMviSj45uy9EADZfsbOP5JPWqtioyhseSNSyB7VBx6Q7946f2K3+en8kgzx3bWUnqgAVebF41OTdqQaEbMSiN1cDSxKeHdNqJHOTIzERlvImdMvFKDP0BjpZ3KI81UHm7i4KZK9q+rwGDWkT0qjvyLkkgdFCWjikKQq81D6f4Gju2uo/JwE35/AHN0GEMmJ5M9Mo7UPnYk3S8TSqvXkDUijqwRcQS+GVAOYffUUbKnjrIDDWh1arJHxzN4YhLpBdHn1eoS3aeh0k7x9mqO7q6l3eZGb9SSPSqOnNHxpBfEoAvrvUNNtVpFfEYE8RkRjLk0A7fTS3lhEyf21VOyu47D26oJjwojf0IiQ6YkE5Mc3mu1iS/yef2UFzZy5OMayg404vP6iYg1MOqSdPLGJRCfERHSreOv0y/D+dNUahVJOZEk5UQy9eo8ak5YObqzlmN7ajm2qxajRc/giUkUyAetV7mdXo7tqqVoWzV1ZTbUWhVZI+LIvyiRzOGxaHWh0fenN2jJG5dA3rgEPG4fZQcaOLqzlv3rKtj7YTnJuZEUTE0hb3xCSPVX9ncNlXYObz/F0Y9rcTo8GCN0DJuewqCLEknMsvTZQP60fh/On6ZSq0jOiyI5L4pp1w7i5KFGindUc2BdBfs+LCcx28LQaSnkjUuQbo8e0lTt4NCmKoo/qsbj9BGTEs60awYxeGISBnNoj2PX6TUMGp/IoPGJtNncHPmohqJtp1j/j8Nse/0YQ6YkM3xGKlEJpmCX2i+52r0c21lD0bZq6stbUWtVZI+MZ8jkJNKHxqDpZ0fAAzaBNFo1OaPjyRkdT5vNzdHT/+gb/lnM1teOkT8hkWHTU4nPiAh2qX1ewB/g5KFG9q+voLK4GbVWRd64BEbMTCMxu2+2ckwWPWPmZjD60nSqS1o4uKmKg+sr2b+2goxhsYyak0Z6QUyffG2hJBBQuiWLtpzi2O5avG4/sWlmpi8dRP6E0P9CvxADNpw/zWTRM/qSDEbNSafmhI3CLVUUf1RD4ZZTJGRZGD4jhbzxiXLYeo7cTi/FO2o4sKECa1075ugwJl6Zw9CpKf3m4iGVSkXKoGhSBkXjaHFRuKWKQ1tO8c6z+4lODmfUxWnkT0yS9845OtPtdWhzFQ0VdrRhGvInJDJ0eioJmX23H/lcqAJfdinVOaisrGTOnDmsW7eOtLS07qor6JwOD0c+rqFwcxXNNW2EmbQMmZTMsBkpRCdJ3/TXaW1ycnBjJUVbT+Fq85KYbWHUnHRyxsT3u0PPL+Pz+CnZU8u+dRU0VNgxhOsYNiOFEbPSCI+UsdNfp7HKzqHNVRz5uAaP00dsqpnhM1PJn5CIvp8Nhe0sO/vXq+1GhnAdoy5OZ+TsNKpLWji0qUoZVrW+gtTB0QyfkUr26LgBETZdVVtmY/+6Ckr21EEgQO7YBEbNSScpp3uvHA11Gp2awZOSyZ+YRHVJC/vWVrDnfyfZ+0E5gyYkMmpOOvHp0l12hs/j5/i+Og5tqqK6xIpGqyZvXALDZ6b22W6v7iDh3IlPH7a22dwUbTtF4ZYq3v/zIUwWPUOnpTB0WsqAvWzc7/NTur+B/esqqD5uRWfQMHJ2GiNnp2GJMwa7vKD69Hunpa6NA+sqOLyjmiMf1ZCaH8WoOelkjogbsBe3WOvbKdxSxeHt1TjtHizxRqZ8I4+CKcn9ui+5q6Rb4zz4/QHKCxsp3FxF2SFlZqnMYbEMnZZC5ojYAdGabre7Kdp6ikObqrA3u7DEGRg5O52CKcn97vCzOzkdHoq2nuLgxsqOv9uIWWkUTEkeELMu+rzKl3nhlioqi5tRqVVkj4pj+PRU0oZED6iLe6Rboweo1aqOi1xsje0c3lbN4W2nWPPHg5gi9QyZlMSQycn9rm/6zJnzws1VHNtdh8/jJ3VwNNOX5pM1cuC2AM+FIVzH2MsyGXVJOif21nNwYyXbXi/h47dPkD8xieH9dIRQY5WdwzuqOfpxDe2tHswxYVy0KJuCKSkyh8lXkHC+QJZYIxOvyGHCwixOFjZRtKWKvR9W8Mn75STlWBg8KZm8cQkYwvtuq8jp8FCyu5ZDW07RWGlHF6ZhyKQkRsxKIzbVHOzy+iSNRt0xZrq+vJWDGys5+lENRVtOkZAZwbDpqcp4+z58FNJmc1Oyp44jH1VTd7JVadSMjGPo9BTSC2Lky7wT0q3RAxxWF0c/ruXwjmqaqx2oNSoyhsWSPyGRzBGxfeICF5/PT0VRE0c+qqF0fwM+rzK+dPiMVPIvSuwTr6GvcbWdHiG05RRNpxxodWpyxsQzZFIyqYOj+sQ0A652L2X76zm6q5aKw80E/AFi08wUTE4m/6JEjBH9Ywhld5BujSAIjwzruEChocLO0V3KpeJlBxrQaNWkD40hZ7TSLRJKb1afz0/VkWZK9tRxYl89LocXQ7iOodNTKJicTFy6ecCeOe8NYSYdI2enM2JWGrVlNo7sqOHY7lqO7qzFGKEjZ0wCeWPjSRkUWkHtsLo4ebCR43vrqSxuwu8LEBFjYMzcDPInJMrR1XmScO5BKtXZSXSmXJVL9fEWTuxt4Pg+ZQImVJCQEUHGsFjSC2JIyIro9Tkl7M0uyosaKT/USMXhJtxOHzqDhuyRceSOTSBzeCwabegEwUCgUqlIyo4kKTuSqdfkcfJgIyWfKN0DhZurCDNpSS+IIXN4LOlDY3p97LTX7aOm1EZFkTI/ckOFHUA5KXxxOjmj40nKtgyok3s9QcK5l6jUZ4dVTb0mj/ryVsoLGykvbGLPmjJ2ry5DrVWRmGkhKTeShEwLcWlmLPHGbuub87h9NFc7qC9vpbrESvXxs6tAmKPDyBufSNYI5QMfKhMPDXRanYbcsQnkjlUmXiovbKTsoPJlWrKnDoDIeCPJeZEk50YRnxFBdLKp2/79/P4ALbVtNFbaqStvpbqkhfryVvy+AGq1iqTcSCYtziFzeCyxqXJk1Z0knINApVKRkGkhIdPC+AXZOB0eTh1rofq4leqSFvavq8DvU04FaPVqopPCscQaiIgzEhET1rF2mcGkQ6NTKR8IlTKHhbvdh9uprAZsb3Zhb3LS2qws9WWtb4fTZxiMETqS85RVINILYohJCe2Jx4Uy8VLumARyxyQQ8AdoqLRTUdxEzXErZQcaKd5RAyjrdUYmmJQllqINmGPCMEeHoTdo0Ru16A0apVUbUEbgeD1+ZS1Ph7KWZ2uTk9YGJ7bGdlpq2vCeXk1arVWRmGVh9CUZJOdGkjIoqk+fsAx18pcNAYZwXcckTABej4/m6jYaKltpqLTTUttOU7WDskONX1h2vTN6o5aIGGVh3DP9f7FpZiLjjRLGfZjqU/NOgxKy1rp2GirtNFYpN2u9slaex+k7p31rdWplya84I6mDozsWsohOCpcurl4k4RyCtDrNZz54ZwT8AdrtHlxtHpwOZdVyvzeA3x8gEFAOM/UGLTqjhjCjlvDIMGnZDBAqlYqoRBNRiSbyxiV85neudi+OFtfpVZ+9uNt9BAIBVCoVarUKtVaFIVx3dgFcs06+uEOAfHL7EJVahcmi7zczuoneEWbUyvqZfZAcowghRAiScBZCiBAk4SyEECFIwlkIIUKQhLMQQoQgCWchhAhBEs5CCBGCJJyFECIESTgLIUQI6nI4+3w+Fi9ezA9/+MOerEcIIQTnEM7/+Mc/yM3N7clahBBCnNalcK6pqWHjxo0sWbKkp+sRQghBF8P58ccf52c/+xlqtXRRCyFEb+g0bTds2EBMTAzDhw/vjXqEEELQhSlDP/nkE9avX8/mzZtxuVzY7Xbuvvtuli9f3hv1CSHEgNRpON91113cddddAHz88cf89a9/lWAWQogeJp3IQggRgs5peYSJEycyceLEnqpFCCHEadJyFkKIECThLIQQIUjCWQghQpCEsxBChCAJZyGECEESzkIIEYLOaSidEEKEooDfj6+5GW9DI76WFuVmsxJoa8Pf3o6/rZ2A1ws+HwGfDwCVRg0aLSqNBpXRgNpgRG00oDabUUdEoLFYlFtsLJrISFS9PLeQhLMQok8IuN24SktxnziB++RJ3CfLcVeU462pxVtbS8Dj+eoHazSodDpUGg1oNMrPfD4Cfr/yOK/3659crUYTHY02IQFtQjy6hES0SYnoklPQpSSjS1ZuKr2+216vhLP4Wv72djzV1XiqqvA1NeGzWvG1WPE77AQ8XqUV4veh0umV1keYAU2kBU1cHNq4eLQJ8ehTU7v1TSv6P397O87Dh3EePEj7wUO4jhTjKi37TIhqExLQZaRjHDMGXWIC2oREtPFxaKKj0URFobFYUJtMqE2mTt9/AY8Hv8uFv60Nv8OBv7UVn61VaYE3NeFtasTX2IS3vh5vXR3OwiJ8DQ2f3YlajS4pCV1aGvrMDHQZGegzMtFnZaLPzERtMJzT30DCWQBKq8R55AjOwiJcx44pt+PH8TU2fnFjlUp5w2u1oNWiUqsJuN34nU4CLtcXt1er0aWmos/MJGxwPoahQzEOG4YuI6PXDxVFaPJZrbTt2UPbrt207dmDs7AQTnc/aBMTMRQUYJ59MWH5+YTl5aLPyEBtMnXb86t0OjQ6HRqzucuP8bvdeGtq8JxSGi+eqkrclZV4yitoXb/hs58dlQptchJhWdnoc3LQZ2fRHhHxtfuXcB6gfHYHbbt30fbxTtr37cNZWEjA7QZAbTIRNmgQ5lkz0adnoEtNQZeSgjYuDk1kJOqICOXw8EsE/H78Nhvehga8DQ14amrwlJfjLivDVVpG2z/+2XH4qY6MxDRuHKYJEzBNmIBhaIGE9QAR8Hpp378fx7Zt2Ldtw3nwEPj9qPR6DCNHEPu972EcNRLD8OHoEhKCXe6XUuv16DMy0GdkfOnvfXb72fd+WRnu0jLcpaVY33oLv8NBbSDwtfuXcB4gAoEArsOHad24EceWrbQfPAher/JhGD6c6OuvxzhqlPJhSE1BpVKd1/Oo1GrlkDIqirC8vC/W4XbjKimhvbCQ9v37adu1C/v69QBoYmIwT59G+IwZmKdPR2OxXNBrFqHFZ3fg2LKZ1g0bcGzajM9qBbUa48iRxN1yC+GTJ2EYORJ1WFiwS+0WGrMZzdChGIYO/czPA4EA3rp6tLt3wZ13fuXjJZz7sYDXS9uuXdjefx/7ho14a2tBpcIwfDix3/0u4ZMnYRwz5pz7wi6ESq/HcPoNG33NNQB4amtp27kT++Yt2DdtxrrqbdDpCJ8yGcvcy4iYczGaqKheq1F0H5/Nhn3DBmzvf4Bj61YCbjeaqCjMs2Zinj2b8MmT0URGBrvMXqVSqdAlJmAcNeprt5Nw7mcCPp8SyO+9R+uHa/G1tKAyGjFPm4Z59mzMM6ajjYsLdpmfoUtMJHLRIiIXLSLg89G+/wCta9fS+v77VG+6n+qHtJhnzCDyikWYZ83q1S8Tce78Tif2jZuwvfcu9o2bCHg8aJOSiLpuKZa5czGOGfOV3WLiLAnnfsJ55AjWVW9je+89vLW1qEwmImbPJuKyuZinT0dtNAa7xC5RaTSYxo7BNHYMCT+7G2dhEbbVq7G9+y729etRm81Y5s8nasnVGEaOPO/uF9G9An4/bbt3Y121itb/vY/f4UATH0f0t75JxLx5GEeNkvMJ50jCuQ/zNjVhe/c9Wla+havoMGi1mKdPJ3LZPZhnz+4zgfxVVCoVxuHDMA4fRsJdd9K2cyfWlauwvvMOLa+9RtigPKKuuYbIK68ccIfGocJdWYX1rbewrlyJp6oKtclExLx5RC66HNNFF0kL+QJIOPcxAZ8Px/bttLz2Oq0bNoDHg2HYMBJ/8QssCxegjY4Odok9QqXRED55MuGTJ5P4wC+wvbealjfeoPbxX1P39DNY5s8n+rqlGEaNktZ0D/O7XLR+uJaWN16nbcdHoFIRPnky8Xf8hIhLLunzjYJQIeHcR3hOnaLljTdpefNNvNXVaKKiiPnWt4j8xjcwDM4Pdnm9SmM2E730WqKXXovz8GGaX30V29vvYF25krChBcR861tYFi6UkOhmzqNHaXntdaxvv43fakWXmkrc7bcRtXgxupSUYJfX70g4h7CAx4N90yaaX3sNx+YtAIRPmULisnswX3wxarnqDkNBAckPP0zC3T/D9u47NP/7Zap/8QC1Ty0n6qqriP7WN79yHKronL+9Hdua/9Hy3//Svm8fKp2OiEsvIWrJEkyTJkk/cg+ScA5B7soqWl5/Desbb+Ktr0ebkEDsLT8k6uol6NNSg11eSNKYw4m+7jqili6lffduml5+maZ//Yuml14ifPo0Yq6/nvDp0yVMush5+DAtr72G9Z138be2os/JIWHZMiIXX9lvu85CjYRziAi43bSu30DLa6/h2L4dVCrMM2YQde01mGfMUC6VFp1SqVQdVxx6auto+e9/af7vq1T88BZ06elKgF/9DRk3/SV8dge21e/R8trrOA8eRKXXEzHvMqKXLsU4dqz05fcy+cQHmaukhJY33sS6ahW+pia0ycnE/ehHRF39DenHu0C6xATib7uVuB/+gNa1a2l6+WXqnnqK+mefVYbjLb0W4+jRAzp0AoEA7Xv30fLG69jW/I9AWxthgwaReN99RF6xSL7EgkjCOQh8ra3Y1qzB+sabtO/fD1otEbNnEXXNNYRPnSrDj7qZSq/HsmABlgULcB45SvMrL589gTh4MFHXXkPk5ZcPqOF4ntparKvexvrWW7hLS1GZTFgWzCfq6qsH/BdWqJBw7iUBrxfH9u1YV66kdd16Ai4X+rxcpR/vikVoY2ODXeKAYBicf/YE4nvv0fzqf6h99FfUPfkUEZdeStTV38A0cWK/7Jv22R20rv0Q2zvv4tixA/x+jOPGkXzzd4mYNx+NOTzYJYpPkXDuQQG/n/Z9+7C9+x62//0PX1MTmqgoopYsIXLxYgzDh0kLJUg05vCO4XjthYVY33gD6zvvYnv3XbRJSURevhDLoiv6/DBFf3s79i1baP3f/2hdv4GA04kuNZXYH/6AqMWL0WdmBrtE8RUknLvZmUBuff99bB98iLe6GlVYGOaLZxO5cKFyck+GwIUU47BhGIcNI+Gee2hdtw7bO+/S+PeXaHzxL+jzcpXJly67jLD8QX3iy9RntWLfupXWtWuxb9pMoK0NTXQ0Ud+4CsvlizCOkW6LvkDCuRv429tx7PgI+4YN2DduxFtfj0qnI3zaNCx3/ATznEvkkLEPUBsMRC5cSOTChcql8WvW0Pr+BzT88Y80rFiBLiMD88yZmGfMwHTRhJCZ2jLg9+M6cgTH9h3YN22ibc8e8PnQxMYSecUiLJddhmnCBBnx08fIv9Z5CAQCuEtKsG/bhmPbdtp27iTgcqEODyd82jQiLr0U86yZ57Sqgggt2pgYYq6/npjrr8fb0EDr2nXYNyhDHZv/+U9UBgPG0aMxjR+PacIEjCOGd+vKHF8n4HbjLC6mfd9+ZfWQjz/G19ICQFh+PrE334x51iyMo0bKyeU+rNvCuequu9AUFBCWnY0+Oxt9Vha6lJR+8W0d8PlwHTtG2+49tO3ZTdvu3fjqlfXD9Dk5RF17LeZZMwmfMEG6LPohbVwc0dctJfq6pfidTmWBgC1baNu1m4bnn4dAANRq9DnZylzVQwrQZ2Upt7TzXz8x4HbjqanBXVGBu6QE57FjuI4ew1Vc3LFqjTYpCfPMmZgmTyJ80iR0SUnd+dJFEHVbcgY8Xmxr/offaj37Q50OfVoa+szMswsepqejS0tDl5oaMoeFn+Z3u3EfP47r6FGch4tpP3gQZ1ERgfZ2ALTJyYRPmozpogmYp06VscgDjNpgwDx9Oubp0wFlMvm2PXtwHirEWVhI20cfY3v7nU89QI0mJgZtXJyyzJfFoiyEazCi0usJ+Lzg9RHwevHbW/G1WPFZrcpCovX1SvCfpomJISw/n+hvfQvj6NEYR4+SMO7Hui2c0579Hampqfiam3GfWS+rrBR32Unc5eU4Pv64I+DO0MTHnV5aPAVdUtLpZccT0MbHo42NQRMbiyYysluHNQX8fnwtLcrCjDW1eGqq8ZwsP73UulLrmYUlVWFhGAoKiLpmCcYRIzCNHYsuVS6fFmdpLBZl3uzZszt+5mtpUd5LZWW4T5YrQXtmTcXKSmUh3PZ2/G43Ko2mY6FcTXi4ssRXXCxh+fnK5yI1FV1qKmF5uTLccoDp1j4HlUqFNiYGbUwMprFjP/O7QCCAt74eT2UVnsoKZZXaU6fwnqrGVVyMfdOmL4Q3oLQ8LBaIZKmuAAAgAElEQVTUFguaiAjUZjNqgwGV0ai0vHVaVGoNKq2GQCAAPj8Bn5eAx6N8ANra8be14bNalWXOW1rA7/9s3UYj+owMwvLyiLhsLob8fMLy89FnZqLS6brzTyQGAE1UFMaoqE6XIRID28aNG7/2990WznV1daSlpX3l71UqFbqEBGUl3bFjvvD7QCCA327HW1en3Jqa8DU24W1qxG+z4bO14mu14W+1421txe904ne2nw5jH3i9oFKBVqOEtU6H2mhEZTIqq0knDOpYeFQbG4s2KVFprScmoU2Il6FFQohec/z4cb7//e+T8TUzJnZbOD/33HP89a9/Pe/Hq1QqNBERaCIiCMvN7a6yhBAi5Dz88MNoOxks0W2duf/5z38oKyvrrt0JIUS/VFhYyL///W9uvPHGr92u28JZpVLxyCOPdNfuhBCiX3rooYcwm83ccsstX7tdt4Xzt7/9bf7xj39w5MiR7tqlEEL0K5988glvvPEGd955J1GdTMfabeH8//7f/8NoNPLQQw911y6FEKJf+cUvfkFMTAx33nlnp9t2WzjHxsZyxx138Oqrr7Jv377u2q0QQvQLW7duZc2aNSxbtgyLxdLp9t06ae3dd99NdHQ0999/f3fuVggh+rRAIMC9995LUlISt956a5ce063hHBUVxbJly1i9ejVbtmzpzl0LIUSftWbNGrZu3cqDDz6IqYsTZHUazi6XiyVLlnDFFVewcOFCnn322a/d/rbbbiM5OZl7771XuWJPCCEGML/fz3333Udubi7f+973uvy4TsNZr9fz0ksv8fbbb7Ny5Uq2bNnytX3KJpOJBx98kG3btrF69eouFyKEEP3Rq6++yv79+/nlL3+J7hymg+g0nFUqFeHhykTxXq8Xr9fb6aXON998M7m5udx33334PzePhRBCDBQej4cHHniAkSNHct11153TY7vU5+zz+bjyyiuZMmUKU6ZMYVQnE7rodDoeffRRDhw4wCuvvHJOBQkhRH/xl7/8hePHj/P444+jPsfZNbu0tUajYdWqVWzatIkDBw5w9OjRTh+zdOlSRo0axQMPPIDL5TqnooQQoq9zOBw88sgjTJs2jQULFpzz488pyi0WCxMnTuzSSAy1Ws0TTzxBaWkpf/rTn865MCGE6Mt++9vfUlNTwxNPPHFes152Gs5NTU3YbDYAnE4n27dvJycnp0s7nzt3LhdffDGPPvpoxz6EEKK/q6+v58knn2Tx4sVMmTLlvPbRaTjX1dVxww03sGjRIpYsWcKUKVOY/alVH76OSqXiiSeeoKGhgaeeeuq8ChRCiL7mV7/6FQ6Hg1//+tfnvY9O53MeMmQIK1euPO8nGD9+PEuXLuWZZ57hRz/6EcnJyee9LyGECHUnTpzgD3/4AzfffDNDhgw57/106xWCX+Wxxx7D7XbLlKJCiH7vF7/4BVqtlocffviC9tMr4Zybm8stt9zCiy++SHFxcW88pRBC9Lo9e/bwyiuv8NOf/pSUlJQL2levhDPQcU35smXLeusphRCi1wQCAe6++27i4+O7Jed6LZzj4+O59957efvtt9m0aVNvPa0QQvSK9957j40bN/LQQw91aUrQzvRaOAPccccdpKWlcffdd8tl3UKIfsPr9fKzn/2M/Px8fvCDH3TLPns1nI1GI4899hi7d+/m1Vdf7c2nFkKIHvOXv/yF4uJifvOb35zT5EZfRxW4wHk9KysrmTNnDuvWrSMtLa3T7f1+P+PGjaO5uZni4mIMBsOFPP0FCwQCWF1WGp2NNLY30uxqxuqy0uJqweay4fA6cLgd2D123D43Lp8Ll8+FN+AlEAgoNwJo1Bq0Ki1atRaD1oBJa8KkNRGuDycqLIqosCgiwyJJMCYQb4onwZSARW85ryuHhAglZz5Dde111LXVUd9W3/EZanG14PA4aPe20+Ztw+l14vV78Qa8+Pw+VKhQqZSbVqUlTBOm3LRhhGvDCdeHY9aZsegtRIZFEhUWRbQhmlhDLLHG2JD4DLW2tpKXl8egQYPYsmVLl+vpLDs7Hefc3dRqNcuXL+eSSy7h2Wef5Z577unR57O77VTZq6iyV1HtqKbaXk1NWw11bXXUOmqpa6/D6/d+6WMNGgNmvZlwXTgmrQmj1ohBa8ASZkGr0qJWqTv+IXx+H76AD4/fg9PrpK6tjnZvOza3DZvLhjfwxecI14WTZk4jLSKN9Ih0ciJzyI7MJicqB4v+wvushOhOVpeVE9YTnGg5wQnrCSpaK6i0V1LZWkm7t/0L22tVWiLDIonQR2DUGjFqjVj0FrRqLRqVBo1aAyjh7gsonx+Xz4Xb58bWZuOk9yR2tx27x47L9+Xz8+jUOhJMCSSaEkk0JZIUnkRSeBIp5hSSw5NJi0gjXBfeo3+XJ598krq6OlatWtWtXxS9Hs4Ac+bMYeHChTz22GN85zvfISEh4bz3FQgEaHG1cNJ2kvLWcspt5ZS3llNhU944La6Wz2wfpgkjKTyJRFMiYxPHEm+KJ94Y3/FNHG2I7mjp6jX6C32pHTXaPXZanC3Ut9crLQxHHaccp6hsraTMWsaWyi24/e6Ox6SEp1AQW8CQmCEMix3GyPiRRIZFdks9QnSm2dnMgfoDFDYWcrjpMMVNxdQ4ajp+H6YJIz0inbSINCYmTSTFnEKCKYEEUwJxxjiiw6IJ14V3W1i5fC5anEpLvNnVTGO7cqTb0N5AXbvS0CpsLGRd+brPfI4AYgwxpJnTSLekkxGRQXpEOhmWDLIsWRf8maqoqGD58uVcd911TJo06YL29XlBCWeAp556ihEjRvDwww+zYsWKTrd3+9yU28optZVSZi2j1FrKSdtJymxl2Nxn5+1Qq9SkhKeQHpHOpZmXkhaRRqo5lVRzKsnhycQYYnr9MEilUhGhjyBCH0G6Jf1Lt/H5fVTZqzhhPUFJSwnFTcUUNxWzrnxdxzZZlixGJ4xmfOJ4xieNJ9Wc2lsvQfRjgUCAytZKdtXuYk/tHvbV7aO8tRwAFSqyIrMYkzCGITFDyIvKIzsym5TwlI6Wb28I04SRGJ5IYnji127nD/hpcjZRba+myl5Fpb2SKnsVFa0V7Kvbx+oTqwlwtic3KiyKTEsmmZZMsiOzybZkkx2ZTXpEOjpN533HZ1Z8+s1vfnPBr/Hzer3P+dNuu+02VqxYwYEDBxg2bBigHDqVWksptZZywnqi478r7ZX4A2dHeCSYEsi2ZJMVmdXxx82IyCDVnNqlP2pf4fA4KGwoZH/9fvbX72df/T6sLiugtK4npUxicspkJidPlpa16LImZxM7Tu1g+6ntfFz9MbVttYDSyhwVP6rjNjR2KCZd19a86wvcPjeV9koqbBWU2co6Gnhl1jLq2+s7ttOoNKRHpJMVmaV0NZ7ucsyOzO7octy5cycTJ07k3nvv5fHHHz/nWjrLzqCEs8/vo9pRzd7SvVw37TpShqUw9aGplFpLaXI2dWynV+vJjMw8+4c5HcZZlqx+9YY5F/6An5KWEnbV7GJXzS52Vu+k1dOKChUj4kcwM20mM9Nmkh+dH/QTJSJ0BAIBDjcdZlPFJjZVbqKosYgAASLDIrko6SIuSrqICUkTyInMGbDvG7vbzknbSUptpR2NwjNH6B6/p2O7OGMcWZYs1i9bT0tVC69ve51hqcNICk9Crer6ALignhC0uqxnv52sZZTZlO6Iclt5R7+QZaGFkv+UkLErg9lzZpMdmU2WJYucyBxSzL176NQXqFVq8qPzyY/O5/qC6/H6vRxqOMT2U9vZUrmF3+/9Pb/f+3uSw5OZkzGHORlzGJMwRv6OA5DX72VP7R7WnlzL+or11LXVoULFyPiR/Gj0j5iaMpWhsUPlvXGaWW9mWNwwhsUN+8zPvX6v0uXYcqIjwza8u4HyA+WkfCeFOz+6E1AGEGRYMjoyLNOSqdxHZp7XCf5uaznf97f7cJgcVLRWUG4r52TryY7Db1DO3KZFpJFlyeroisiJzCHFkMK0cdPQ6/Xs37+/28YIDlQN7Q1srtzMhvINbD+1HbffTYwhhjkZc5iXNY9xiePkw9iPef1edtbs5P2y91lfvp4WVwsGjYGpqVOZnT6b6WnTiTHEBLvMPs3pdFJQUEBERARrt6+l3H72XNiZLpIqexW+gK/jMdFh0aRb0smMyOw4MRlmD+PH1/y457s1dD/SoY5SkxSeRIYlg8yITOX+9LdHakQqOvWXB++qVatYvHgxzz77LLfddtuFlCM+pc3Txuaqzaw9uZbNlZtp97YTZ4xjbuZcFuQsYGTcyAF7CNuf+AN+5WRX6Wo+PPkhTc4mwnXhzEybyaWZlzI1dSpGrTHYZfYbjz/+OPfffz/r1q3j4osv/tJtPD4PFfYKTlpPctJ2kpOtJ5VGq+1kR/9+oCWAZ4Wn58P57yv/zrj8cec1/CwQCDB37lz27NnDsWPHiI2NvZCSxJc4E9QflH3ApopNuP1u0iPSWZC9gMtzLicrMivYJYpzdLzlOO8cf4c1pWs45TiFUWtkZtpM5mXNY1raNMI0YcEusd+pqqpi8ODBXHbZZbzxxhvntQ+n10mVvYr9Jfu59/p7Q+uE4Jc5dOgQo0eP5pZbbuG55567kJJEJ1rdraw9uZb3St9jZ/VOAgQYFT+KK3Kv4LKsy2TURwhrcjaxpnQNbx9/m6LGIjQqDZNSJrEweyFzMuYM2BPlveWGG27gv//9L0VFRV1eru+rhORoja9y66238oc//IF9+/YxYsSIC9qX6JpaRy2rS1fz9vG3KWkpQafWMTt9NlfmXcmUlClo1UEbCi9O8/g9bKncwqqSVWyu3Iw34KUgpoBFuYuYnz2fOGNcsEscED766CMmT5583kPnPq9PhXNjYyODBg1izJgxrF27VvpDe9GZoVbvHH+H9068R7OrmThjHItyFrE4bzE5URfWShDn7kjTEVaWrGR16WqanE3EGmJZlLuIRbmLyI/OD3Z5A4rf72fy5MlUVFRw5MgRIiIiLnifITe3xteJjY3ll7/8JbfddhsrV67kqquuCnZJA4ZKpWJo7FCGxg7lznF3srlyMytLVvKPon/wt8K/MTJuJFfmXcn87PlE6C/8jSm+nNVl5b0T77GyZCWHmw6jVWuZlTaLxXmLmZI65StPqoue9c9//pOdO3fy97//vVuCuStCquUMyryoY8eOxWazUVRUhMkkfWjB1NDe0BEWJS0lhGnCmJMxhyvzrmRi0kQZltcNvH4vO07tYGXJSjZUbMDj9zAkZgiL8xazIHsB0YboYJc4oFmtVvLz88nJyWHbtm2o1d0z03KfajkDaLVafv/73zNr1iyefPLJC14kUVyYOGMcNw67kRuG3kBRYxFvlbzF6tLVrC5dTaIpkctzLueKvCvIiZRuj3N1rPkYbx9/m3dPvEtDewPRYdEsHbyUxXmLGRwzONjlidMeeeQR6uvrWb16dbcFc1eEXMv5jG9+85usXLmSw4cPk5WV1W37FRfO5XOxsWIjq0pWse3UNvwBP8Njh3N57uXMy5pHrFGGQn6V+rZ6Vpeu5t0T71LcVIxWpWV62nSuzL2SGWkz+tW8MP1BUVERo0aN4qabbuKFF17o1n33qROCn9/vmfGEb775ZrftV3Svz4eNRqVhcspkFmQv4OKMi3t8Lt2+wOa2se7kOtaUruHjmo87vswW5ixkQc4CuWIvRAUCAS699FI++eQTjh49Slxc946K6XPdGmekpaXxwAMPcO+99/L+++9z2WWXBbsk8SXiTfHcOOxGbhx2I8eaj/HuiXdZU7qG+7beR5gmjBlpM5ibOZcZaTMG1BjcVncrmyo38UHZB2yt2orH7yHNnMbNw2/m8tzLpRuoD3jjjTdYt24dzz33XLcHc1eEbMsZwOVydYx3PnjwIGFhcsVTX+AP+DlQf4DVpav5oOwDGp2NhGnCmJIyhTkZc5iRNqNfnuQ6M6/JuvJ17Di1A4/fQ4IpgcuyLmN+1nyGxw2X4aF9hN1up6CggJiYGPbs2YNW2/3t2D7bcgYICwvj97//PfPmzWP58uXcf//9wS5JdIFapWZ0wmhGJ4xm2YRl7Kvfx4cnP+TDkx+yoWKD8vv40UxPm87UlKkMjhl8TlMthgp/wM/hxsNsO7WNTZWbOFh/kAABksOT+eaQb3Jp5qWMjB/ZJ1/bQPfoo49SWVnJq6++2iPB3BUh3XI+Y8mSJaxevZqioiI5OdiHBQIBipqK2FixkY0VGyluKgaUCd4np0xmQuIExieNJyMiIyRbmIFAgFJrKbtrd7O7Zjc7qnd0LIM2LHYYs9JnMTt9tsyl3cedOQn47W9/m7/+9a899jx99oTgp1VUVFBQUMCcOXNYtWpVjzyH6H31bfXsqFZW49hxakfHQgtxxjhGx49mWNwwhscNZ2js0KAseGt1WSlsLORQwyEONRxif/3+jhrjjfFMTpnMlJQpTEqeJCNU+olAIMDFF1/Mvn37OHr0KPHx8T32XH26W+OM9PR0HnzwQZYtW8a7777L5ZdfHuySRDeIN8VzRe4VXJF7hdIqtZWyp3YPu2t2c7DhIGvL13Zsm2hKJC86j7zIPDIsGaSZ00iNSCUpPOmCZl9zep1UO5T15qpaqzjZepLjLccpaS6hrr2uY7ssSxZTU6YyPmk84xPHkx6RLq3jfuiVV15h48aNrFixokeDuSv6RMsZwO12M3r0aNrb2yksLJQrBweAFmdLx+rPJS0lHG85zomWE19YXdmsMxNjiCHaEI1Ja8KoNWLUGdGqzrY9vAEv7Z522r3tOLwOmp3KCs5t3rbP7MugMZAdmU1eVB65UbkMjR3KsLhhQWm5i95ltVoZMmQIaWlpfPTRR2g0PXv1a79oOQPo9XpWrFjB7Nmz+dWvftUts0KJ0BZliGJq6lSmpk7t+Jk/4KeurY7K1koq7ZXUt9XT5Gyisb2RZlczDq+DBmcDbZ62zywIrFFpMOqMmLQmwrXhpMalEmuIJdYYS4IpQWmJm1OJN8XLCbwB6v7776euro533nmnx4O5K/pMOAPMmjWLG2+8kaeeeorrr7++Y8VuMXCoVcpqO0nhSYxnfLDLEf3Ezp07WbFiBbfeeivjx4fG+6rPNRGeeuopLBYLt9xyC36/v/MHCCHE1/B6vdxyyy0kJSXx6KOPBrucDn0unOPj43nyySfZunUrf/vb34JdjhCij3vuuefYu3cvv/vd74iMDJ1VgPpcOAPcdNNNTJs2jXvuuYf6+vpglyOE6KMqKyt54IEHmD9/PkuWLAl2OZ/RJ8NZrVbzxz/+kdbWVu68885glyOE6IMCgQC33norPp+P5557LuSGRvbJcAYYNmwYy5Yt41//+hcffPBBsMsRQvQxb731FqtWreKRRx654MVae0KfDWdQhr7k5+dzyy230NbW1vkDhBACaGlp4dZbb2X06NH89Kc/DXY5X6pPh7PBYOCFF16gtLRUVkwRQnTZz3/+c2pra3nxxReDNrFRZ/p0OAPMnDmT733vezzzzDPs3bs32OUIIULc1q1b+dOf/sQdd9zBuHHjgl3OV+o0nKurq/n2t7/N/PnzWbhwIS+99FJv1HVOnnzySeLi4rj55pvxer3BLkcIEaKcTiff//73yczM5Je//GWwy/lanYazRqPh5z//OWvWrOHVV1/l5ZdfpqSkpDdq67Lo6Gief/559u7dy/Lly4NdjhAiRD366KMUFxfzwgsvEB4e2kuodRrOCQkJHZdJm81mcnJyqK2t7fHCztXVV1/N1VdfzcMPP8yRI0eCXY4QIsTs3buXJ554gptuuom5c+cGu5xOnVOfc2VlJYcPH2bUqFE9Vc8Fee655zCZTNx8881yabcQooPH4+G73/0u8fHxPP3008Eup0u6HM4Oh4Pbb7+d++67D7PZ3JM1nbekpCR++9vfsm3bNlasWBHscoQQIWL58uXs27ePFStWEB3dN9av7FI4ezwebr/9dhYtWhTyhwM33HAD8+bN4+c//zmlpaXBLkcIEWRFRUU88sgjXHPNNVx11VXBLqfLOg3nQCDA/fffT05ODjfddFNv1HRBVCoVf/rTn1Cr1dK9IcQA5/V6+c53vkNERATPPfdcsMs5J52G8549e1i1ahUfffQRV155JVdeeSWbNm3qjdrOW0ZGBs888wwbNmzgD3/4Q7DLEUIEyfLly9m1axfPP/88CQkJwS7nnHR6acz48eP75OiHm2++mddff5177rmH+fPnh+S180KInlNYWMhDDz3EkiVLuPbaa4Ndzjnr81cIfhWVSsWf//xntFot3/3ud6V7Q4gB5Ex3hsVi4fnnnw92Oeel34YzKKt2P/PMM2zatKnP/gMJIc7dE088we7du1mxYkWf6844o1+HM8B3v/tdFixYwLJly/pk94wQ4tzs3buXhx9+mKVLl3LNNdcEu5zz1u/DWaVS8eKLL2I0Grnhhhtk7g0h+jGXy8UNN9xAfHx8nz9a7vfhDJCcnMwf/vAHdu7cyRNPPBHscoQQPeTBBx/k0KFD/OUvfyE2NjbY5VyQ0JzItAdce+21vPXWWzz88MMsWLCAMWPGBLskIS6Muw3am8FlA1ercu91gdep3PvcEPCD36dsr1KDWgMqDWjDTt8MoDOC3gxhEcrNEAU6Q3Bf23nYunUrTz31FD/4wQ+YP39+sMu5YAMmnAGef/55Nm3axP/93/+xe/dujEZjsEsS4ov8frDXQPNJaDkJLRXQegps1dBaDY4GaGsEb3vP1aA1KCFtioXwOAiPV24RiWBOUu4tqWBJUQI9yGw2GzfccAPZ2dl9Zu6MzgyocI6JieHvf/87l112GcuWLePZZ58NdkliIPN5oekE1BVCbRE0HIXGEmg8/sXgNcVCRDJEJEHCUAiPVX5mjIYwy+mbWWkFaw1Kq1itO91SVgOq061oLwR84HWfbWF7HOCyg9uutL6dVmhvUVrlbU3gqIdTn4C9HtytX3wdYZEQmQqR6RCVAVHpEJ0FUZnKvTGqx/+Ut99+OydPnmTz5s0hO/fPuRpQ4Qwwd+5cfvKTn/C73/2OBQsWMG/evGCXJAYCnxfqD0PVJ1C9D07tg9pC8LmU36vUSpDFDoLsmRCbczbgItNDp5vB7YDWmtO3arBWgu0UWCuUFn7FR0q4f5ohCmJyICb79H0uxOYq96YYuMBVr1977TVeeuklHnjgAaZOnXpB+wolqkAgELiQHVRWVjJnzhzWrVtHWlpad9XVo5xOJ+PHj6exsZEDBw4QHx8f7JJEf+O0QcVOKN+u3Fd9orRQQWlpJo+E5FGQOBwSh0Lc4NAJ4AvltCpdMs1lZ29NJ6C5FFrKlRb8GYYoiM07e4vLU76gYnOVo4BOVFZWMnLkSAYNGsTWrVvR6XQ99aq6XWfZOeBazqAsDPvyyy8zYcIEvv/97/PWW2+husBvbzHAuR1wcgeUboSyrVC9XwkhlQaSRsCY6yHtIkgdq7Qe+/P7zXDmy2fkF3/ndSv96I3Hoem4ct9YAmVb4MB/PrWhSukeiR0EcYNOB/cg5f8tKaBS4ff7+c53voPL5eJf//pXnwrmrhiQ4QwwcuRIfv3rX3PXXXfxwgsv8MMf/jDYJYm+xO+H2oNQshZK1imtY78HNHolhGf8DDKnQNoE0If2cki9SqtXQjZu0Bd/53YoQd1w7FP3x+CTj84edQDowiE2l6e3OVm3bjcvPPhDBoU7lBErIXBysrsM2HAGuOOOO3j//fe54447mDZtWsdyXEJ8KacNTmyAo+/DsQ/BUaf8PGkkTP4R5MyC9EmgNwWzyr5LH6509SR/bqWlQEDp32441nHSdNfOndz38m6uLtDyPV6GF15RtjUnne4iyVXuY3KU/47O7nPdRgM6nNVqNS+99BKjRo3iuuuuY+fOnTK8TnyWtQqOrIbi95TuCr9HOWzPuwTyLoXci5VhZaLnqFRKV4YlBXJmYrPZ+OZtY0lOTefPGz9CFWhRWtgNx5S+7cYSKH5XGW54difK0L+YbOUWna2ccD1zM0aHXFfTgA5nUJa2eumll5g/fz533313n7/kU3SDhhI4vAoOvwOn9io/i82DSbdA/nxInwiaAf/RCZof//jHlJaWsmnTJqITUoAU5aTq57U3nw7rE0r/dlOpclLyyBpleOCnhVlOD/07PTom6vSwwMh0iExThi32cnjLOwyYN28ed911F08//TSXXnopixcvDnZJorfVHYbClVC0ShnyBpAyFuY8BEMuh/j84NYnAPjnP//Jv/71Lx5++GGmTZv29RsboyF1nHL7PJf9s6NJWk4qI0waS+D4hs/2cYMydtySqoznPnPxTUTyp25JYE4ATfedlByQQ+m+jNvtZsqUKRw/fpx9+/aRmZkZ7JJET6srhsK3lFvDEUClnMQruAIKLldaTCJkFBcXM378eMaOHcv69evRanuobRkIKK3uM1dn2qqU8dxnxnTbTil94AHfFx9rilX6vc3xEJ6gBHZ4HJjOXGUZp4ztNsZQ2dDKnEsukaF0ndHr9bz66quMHTuWpUuXsnnzZvR6fbDLEt2toQQK31QCua4IJZCnwkXfh4JFSgtIhJz29nauvfZajEYjr7zySs8FMyjdF6YY5ZbyFXPw+H1K10hrtXJBju0U2OvAXnv6Vqd0qdjrv/oy+zY9EPOVZUg4f0pubi4vvvgi1157Lffddx/Lly8PdkmiO7SUK2F86A1l/DFAxmSY/xQMvUICuQ/4yU9+wsGDB1mzZg2pqanBLke5LD4iqWvvHZcd2hrA0ajctzUql8VXVsCqlV/5MAnnz7nmmmv40Y9+xNNPP82sWbO4/PLLg12SOB+ttVC0Ugnkio+Vn6WOg7mPwbDF0mXRh7zyyiv8+c9/5uc//3nfnG4hzKzcorM++/PKSkDC+Zw8/fTTbN++nRtuuIG9e/dK/3Nf4WiEw28rgVy2FQgol0fPeRCGfUMZQuFbrpoAACAASURBVCX6lOLiYn7wgx8wdepUHn300WCX06u6L5wL3wJ77tkpBk2xynjQEBs72BUGg4HXXnuNcePGsWTJErZu3UpYWFiwyxJfpr1ZGYN86E0o3aTMuhY7CGbeowRywpBgVyjOk8PhYMmSJRgMBv7zn//0bD9zCOq+V/vhQ2D+3NlLte7sXLDmBDAnfuo+8ewQlIjkkLt6Jy8vj5deeomrrrqKn/70p6xYsSLYJYkz2puVsaqFK+H4euXCkKhMmHwrDL9amcuiDzYKxP9v776jo67Sx4+/p2YmZdILLYHQIQSRoiIGlBBKAIFQxMAiR0RZDyq49nV1QVyFr1lRf8oBWRCXRaWEJiEgGkBQQ1k3dKWGEAikl6mZmd8fn0kzkUQI+aTc1zlzhmQyM0/CzPO5cz/PfW4Fp9PJk08+ycmTJ9m1a1eTrgS7VfWXnGcmgY/GNdmd42oIni2d0Sy+IS11vX5KOovpsFW/v96vYhWQobU0J+jdTqop9HFd12MNYV2MGzeOF154gSVLlnD//fcTHx/foM8vVFKSA2e+hpNb4XyK9Brybgf3PAkRE6SaZJGQm41ly5axdu1aFi5cSHR0tNzhyKL+krN3G2hTh6ObwyGNfIor9YQt2+GhMFOqKbxy5DdLL5H63Xq1kt6QvmEVq3nKll96tQZl/W+J+Pbbb/PTTz8xe/ZsevfuTURERL0/h/A78i9LS6dPbYNLB6Qubz6h0kq9HuOlDm8iITc7qampPPfcc4waNYpXX31V7nBk0/CTOEqltIuDhz8E36TRkM0kJev8dKn4Oz/d1dA7HS4egKL1VfvCqrRSwvYLr3rxDwfv0FtebqtWq8vrn8eNG8ehQ4fw9fW9pccSauFwwLX/SY2FTn8N19Kk7wd0gUHzpbK3kEiRkJux69evExcXR6tWrVizZg3KOzDgaioa7wy7Ru/qLNWx5ttLrVCYUamZt2vdfO5F6Ux95eWXSrU0uvbrWLVjVUBnaTRey5s9JCSEDRs2MGTIEKZNm8a2bdta9IumXpkL4PxeOLsbftklfaJCIbXajP47dIutub2k0OzYbDYmT55MdnY2Bw8ebPK7Z9+uxpuca6PWVoyOf8vpdK3QOedqfFKpsfeFfVVX7Gg9Xcn6t029O1Xpwztw4ECWLl3Kn//8Z958800WLFjQAL9kM2S3SbuCXNgrncy7nCotg3UzSB3euoyAzsOkE8lCi/LCCy+wd+9ePv/8c/r0+Z2VeS1I003ON6NQSG0cvYKlXgmVORzSTsa/beqdkSrVx1Kp1YihjStZd4GAzjwV3ZlD8ZNYuHAhffv25eGHH27QX6tJstuk/fIuHYBLB6VrazGgkHbKGPSc1H6zbf8GP+ErNB7//ve/Wbp0Kc8++yzTpk2TO5xGoXkm55tRKl2VIG2l5uiV2UzSSLtsB4Zs1yXtS7AUogA+bu/kWBs106ZM4Me3RtGzT/+qG1Z6BLTsOdHi65BxWDrYZRyWTu7ajNJt/p0gcrK0gWmHKKl3gdDiHTp0iCeeeIKoqCiWLFkidziNRstLzjej0UsnKX97otLplJqZ5JxFl/0rid2O0n/up4x9Zxeps77HX1fpxKSbd0VDb79wV1NvV1WJoY20Jr85cDikOf7rJyHrZMWO0kWZ0u1KtWvvvOnSp5ewgVKNuyBUcvXqVcaNG0dwcDAbNmxodvsA3g6RnOtCoahoctJ+EG37zSSxUzyDBw9mcmofdv7nYzSF6RXz2rnnpQY7J7dWbSuoVLvqtis18a7cH9YzpF62iq83DodUn553qWJTzpxKU0FlI2IU0jx9+0HSFkNt7oZWd4ntmoSbMpvNjB8/noKCAg4ePEhgYKDcITUqIjnfonvvvZfly5fz2GOPMX/R/+PDDz+s/kN2m6sMsNI28fmXpZLA8ylSZULlckCQVlV6Brv6wQZKfWDd/aTG4Xpf0PuA1ktqpKL1BI27tLpSrZPmbBUq6SCgVEmP7XRI7Q0dNii1QKlZmr6xFEl74lkKwZQrdcky5kjTEkVXK+rP7ZZKwVXaEfnugdLuE0E9pSXSYhNT4Q9wOp089dRT/PTTT2zcuJHIyBp26m7hRHK+DTNmzCAtLY2EhAR69OjBnDlzqv6ASlMxxVETu02aLim4Ii2+Kc5yLcy5Jq2uLM6CrBPSop3yUeod5OYt1Z97tZZO0HmFSLXjPmHSaN83TJr6EYTbtGTJEj777DPefPNNJkyYIHc4jZJIzrdp8eLFnDlzhrlz5xIeHs7w4cPrfmeVpuLkZG1sZjDngylfqnawFEp9YkvNrotFujjtUvMfp0NaVVl2UWlB7QZqvTTSdvNyjcC9yndmQC02FxDuvMTERF5++WWmTJnC3/72N7nDabREcr5NKpWKdevWMWjQICZPnswPP/xAjx41bDZ5uzQ60NSxubcgNFJHjhwhPj6ee+65h1WrVqFoLOdXGiGxzK0eeHl5sW3bNvR6PaNHj+b69etyhyQIjc6VK1cYO3YsQUFBbN68Gb1eTJHdjEjO9SQ0NJRt27Zx7do1xo4di9HYAHPEgtBEFBYWEhsbS1FREdu3byc4OFjukBo9kZzrUf/+/Vm7di2pqalMmzYNu72G3XkFoYWx2WxMnDiREydOsGHDBtHZsY5Ecq5n48ePZ+nSpSQmJvL888/LHY4gyKqsaf7u3btZvnw5MTExcofUZIgTgnfA3LlzuXjxIgkJCYSFhTFv3jy5QxIEWSxYsIBVq1bxxhtvMHPmTLnDaVJqTc6vvPIKKSkp+Pv7s3379oaIqVlYsmQJ6enpzJ8/n5CQEKZOnSp3SILQoJYvX86bb77JjBkzeOONN+QOp8mpdVpjwoQJfPrppw0RS7OiVCr5/PPPGTx4MDNmzGDXrl1yhyQIDSYxMZE5c+YwcuRIVqxYIUrmbkGtybl///54e3s3RCzNjk6nY8uWLfTo0YMJEyZw6NAhuUMShDtu3759TJ06lQEDBrB+/XrRzOgWiROCd5i3tzdJSUkEBQUxatQoTp8+LXdIgnDH/O9//2Ps2LF06NCB7du34+Eheq7cKpGcG0CrVq1ITk5GqVQybNgwLl26JHdIglDvfvnlF2JiYvDy8iI5ObnFbzN1u0RybiCdO3dm9+7dFBcXEx0dzbVr1+QOSRDqTXp6OtHR0TidTr755htCQ0PlDqnJE8m5AUVGRpKUlMTVq1eJiYkhNzdX7pAE4bZlZWURHR1NYWEhu3btomvXrnKH1CzUmpznz5/PI488woULF4iKimL9+vUNEVezde+997JlyxbOnDnDiBEjKCgokDskQbhl2dnZREdHk5mZSVJSEnfddZfcITUbtdY5JyQkNEQcLcrQoUPZuHEjEyZMYOTIkSQnJ+Pl5SV3WILwh+Tm5jJs2DDOnj3L119/zX333Sd3SM2KmNaQyejRo/nyyy9JTU0lNjaWkpISuUMShDrLz88nJiaGkydPsmXLFh566CG5Q2p2RHKW0fjx4/nPf/7DgQMHGDNmjEjQQpNQUFDAiBEjSEtLY9OmTaJfxh0ikrPMJk+ezJo1a9i7dy+xsbEUFxfLHZIg/K78/HyGDRvGkSNH+Oqrr4iNjZU7pGZLND5qBOLj41EqlUyfPp2RI0eyY8cOMQeN1NHMaLVTbCml2FJKiaWUEosds82OySZdW0odWEsd2OwOrHYHDoeTUocTh8NZ7fGUSgVqpQKlUoFWpUSrVqJRKXFTK9FrVOhcF083NR5uKjzc1Hjp1Og1KrH8GGmOOSYmhrS0NDZu3MjYsWPlDqlZE8m5kZg6dSpqtZqpU6cyfPhwkpKSmt2yebPNzo0iCzeKLdwospBTbCWn2EJOiZXcEiv5JhsFRit5RhuFZhtF5lLsNSTZuqqcT523/jColAoMOjUGvQYfdy0+eg0+7hr8PLT4e2jx93TD30NLoJcbgV5uBHi6odOobv0JG6Hs7GyGDRvGyZMnSUxMFCPmBiCScyMyadIkVCoVU6ZMYejQoezcuZOAgAC5w6qTQrONq/lmMvNNZBaYuJpv5mqBmazCikuhubTG+3q5qfH10OLrocXHXUv7AA+89Rq8dGoMOg2eOrU0mtWqcdeq0LsuOrUKN40SrUqJRi1dq5QKVAppdPxbDocTu9NJqd2JzSGNuMsuZSNxk9VOidWO0SqN1ovMpRSZbRSaSikw2cg32cg3WjmfXUxeiY1iS82/k7deQ7DBjWCDjhCDjlbeOkK89bTy0dHGR09rHz2ebk3j7Xf16tXyqowtW7YwYsQIuUNqEZrGq6MFmTBhAps3b2bixIkMHjyY3bt307p1a7nDosRSSnqukcu5Ri7nmbicayQjz0RGnpEreSaKfpOklAoINugINujoGOjJwI7+BBl05aPLQE9phOnrocFN3TCjTKVSgRIFGhXoqZ/nNNvs5BmtZBdZuVFsJrvIyvUiM9eLLGQVmrlWaOHXrGyuF5n57YcAg05NW1932vrqy69D/dxp5+dOOz897lr5354XLlwgOjqarKwskpKSePDBB+UOqcWQ/39fqCY2NpakpCTGjBnDAw88wDfffEOHDh3u6HM6nU5yS6xczDFyKaeEizlG0nNKuJRrJD3HSE6JtcrPe2hV5QllQAc/2vjoaeMrjQhbeesI9HRDrWr+55t1GhWtvPW08tYDvz8NVWp3cL3IwtUCE1dcnzCu5Jm4km/iYk4J35/Nxmituq1ZgKcbYf7uhPq5E+bvTnt/j/JrH3fNHZ8HP336NNHR0RiNRvbs2cM999xzR59PqEok50ZqyJAh7NmzhxEjRnD//fezc+dOIiMjb/tx80qsnM8u4WJ2CRdzSrjgur6Ubawy+lUqoJW3njB/d2J6BtPOT0oSoX7utPN1b5Dk0JyoVUpau6Yz+oZVv73s4Fj2qSTddVBMzzXy0/kcNv98pcq8uUGnpn2AB+39PWgf4EGHAClphwd44u1++y06U1NTGTVqFGq1mpSUlHp57Ql/jEjOjdiAAQPYt28fI0aMICoqiq1btxIVFVXr/UospeVJ98INKQGfz5auC0y28p9TKqCtrzvtAzzoG+pLmL8H7QPcCfP3oK2vvsGmGwRQKBTSiUVPN+5q51PtdrPNTkaeqfygeinHyMWcEo6m57EtLbNK4vZ119AhwIMOAZ6EB0oJvEOA9H9bl6mS5ORk4uLiCAoKIjk5mc6dO9fnryrUkUjOjVxERAQHDx4kJiaGmJgY1q1bx/jx47GU2knPMXIhu2L0e96ViK8XWao8RmtvHe0DPBgd2Up6k/p70CHQg3a+7mjVzX/qoTnQaVR0CvKkU5BntdsspXYu5xo5f6Ps05CRC9nFHDibzcajGVV+NsSgcyVqD8IDPMr/HeonvRbWrl3LY489Rs+ePdm5cychISEN9SsKvyGScyMmvelMXCx248kl/+a9vzxOXNxEOox5GkeP4VVGS/4eUpVDVJfA8gRcNmrSa8UIuDlzU6voFORFp6DqtfElltKK6atKn6B2Hr9KnrHiU5QCJ87/beHSzk8Ji+jPrHdWcDJfQYmqWBzEZSKSs8wKzbbyucVLOUbSc6WPrJdyjGQWmKokYO+4BZRu/z/Ob/2QKFUhz7y6gE7BhvLSM0H4LQ83NT1be9OzdfWTlflGKxeyS/j1aj7//PtL/LhzPa37RuMx/Bn+LyUDkEbdSgW09pHOP4T5exDmOkEZ6udBOz89Xjrx2rsTRHK+w0xWO1fypfKzjDwTGblGLudJZWjpuUbyK41eAPw8tIT6udO/vS9h/m1pHyC9CToEeODrrsGxcDTz58/ngw8+wM9ZwNq1a3EXiVm4BT7uWjr6mHll9hx+TE7mtddeY8GCBSgUCnJKrFzMLhsolJRX8SQdqzriBuk1285XT1vXyeJ2flJpYBsfPW199c1uQU5DEcn5NpTaHWQXW7laYCIz31x+nZkvlUhl5puqlaBpVUqprtXPnci23hUVEK7r2kYhKpWKpUuXEh4ezrx584iKimLLli20adPmTv6qQjN0/vx5xo4dy+nTp/n00095/PHHy28LcNWh92vvV+1+BSZbRUWJ6xNfRp6RE1cK2HXiGjZ71YLuAE9t+cKb8ou3jlausssATzdUNSwaaulEcq6B3SGVNZUtNb5eWLGooGxhQVaBucaFBXqNqrzeN6KNt2uBgd41inAnyMutxtVrf9Szzz5Lx44dmTp1Kv369WPz5s2iDlWos7179xIXF4fD4SA5OZmhQ4fW+b7eeg3ebbyJaFN9qsTucJJVaOZKvrRAKSNXWjGakWfiTFYR3525jtnmqHIflVJBkFfFasoQbx1BBjeCvHQEebkRZJAWLfm6a+vlvdNUtIjkXGp3UGCykWe0kWeU+jjklVjLezqU9Xe4UWQhu9hKbomlWtIFqbY0xFta9dY5KMC1JLdsea6e1j46vPUNV/87evRofvjhB8aOHcvgwYNZuXIl8fHxDfLcQtO1fPlynn76aTp16sTWrVvrtVROpVSUj4771zDqdjqd5Btt5Uv8rxWauVZgJrPAxPVCC2dvFHPgXDZFNSz1VykV+HloCfR0w99TS4Crp4mfp9TjxNddi5+rDYCvuxZvvaZJj8gbfXJ2Op1YSh3lXcnK+h0Um6V/lzXIKTTbKDRV9ECQ+iBYyTfaavyPLqPXqAjw0uLv4UZbXz13tfOp0sAmyEs6ggd6uTXKqoeIiAhSU1OZOHEi06ZN4/DhwyxevBiNRsxDC1VZLBbmzp3LihUrGDFiBF988UWDN9dSKBTlfVRqOklZxmgt5UaRhetFFq4XWrhRZCa7uOLTbE6JdDIzu9hSbSRemUGnlppVuWvw1msw6DUYdBoMeqlvi0Gnxksn9XHxdFNX9HFxk67d1ErZFlvVW3I+c62ILHsu1lInVrsDi82O1S41lbGUSl+bSx3lbR7NlRrNmGx2jFbpa6NV+p7RaqfEWorRaq9TZzKtWolBp8Fbr8Zbr8HfU0unIE/pI5heg6+7pvyI6usuHW393LWNMuH+UQEBAezevZsXXniB999/n6NHj/Lll1+KGlWh3OXLl4mLi+PQoUO8+uqrLFiwAJWq8b723bVqwvzVhPl71PqzJqudnBKL9InYaCOvxEpeWXdDV6Oqsk6HV/JNFJpKKTTZsNp/P6mXUSsV6LUqqemWm0pqvKVRodeqcde4GnBpVOg0SulaLf3bTa3ETaOSrtUqtGqpRW1Zq1qtSkl+9s0316i35Pz4Z4fBo/rHmJpoVUrcNErXL+n6hbQq3DUqQgyaan+MsqOYh1Y6ohl0FUc4g6t7WUtfzabRaHj//fcZMGAAs2bNom/fvnz55ZcMGjRI7tAEmX3zzTc8+uijmM1mEhMTGTdunNwh1Su9VkVbrTttfd3/0P3MNnv5p+4Si/RpvNDs6htureghbrTaMVqkwWLZwLHAZCOrwIyprLe41Y651F7tZOhNleTidpOb6y05vxPXi1at26BRKXBTK9GqpKOFdBSRjiDS16omPQ/U2D366KNEREQQFxfHkCFDeOutt3jxxRdRKsUigpamtLSUv//97yxatIju3buzadMmunbtKndYjUbZ5gqBXjdLkX+M3eEsnx2wlNqx2BzlG0JY7dL3bXYn1lIHWVevsHDX7z9WvSXnQZ0CaNs2sL4eTrgNkZGRHDlyhNmzZ/PKK6+QkpLCmjVrCAoKkjs0oYFkZmYydepU9u3bx8yZM/nwww/x8Kh9ikC4PSqlAg83NR51yPcZBhsLb3K7GE41UwaDgXXr1rFs2TJSUlLo3bs3O3fulDssoQEkJiYSGRnJ4cOH+eyzz/jXv/4lEnMTJJJzM6ZQKHjyySdJTU3F39+fkSNH8uyzz2I2m+UOTbgDiouLeeKJJ5gwYQJhYWEcOXKEP/3pT3KHJdwikZxbgMjISA4dOsTcuXP54IMP6NevH0ePHpU7LKEeHTx4kLvvvpuVK1fy0ksv8cMPP9CtWze5wxJug0jOLYRer+eDDz4gKSmJvLw8BgwYwOuvv47Vaq39zkKjZTKZ+Mtf/sKgQYOwWq18++23vPPOO2i1WrlDE26TSM4tzIgRIzh+/Djx8fG89dZb9OvXjyNHjsgdlnALDh48SJ8+fXjvvfeYPXs2x44dY8iQIXKHJdQTkZxbIF9fXz777DO2bt1KdnY2AwYMYN68eRQVFckdmlAH+fn5PPXUU9x///2YTCZ2797NsmXL8PKq3s9ZaLpEcm7BxowZw6lTp3jyySdZunQpPXv2ZMuWLTidf6CQXmgwTqeTr776iu7du7NixQrmzZvHiRMniI6Oljs04Q4QybmF8/b25uOPP+bAgQN4e3szbtw4YmNj+eWXX+QOTajkxIkTDB06lClTptC6dWtSU1NJSEjA07P6tlVC8yCSswDAfffdx9GjR0lISODAgQNERETw8ssvU1hYKHdoLVpeXh7z5s2jd+/e/Pzzz3z88cekpqbSt29fuUMT7jCRnIVyGo2GefPmcebMGeLj43n33Xfp1KkTH3/8MTabrfYHEOqNxWIhISGBjh07snTpUmbNmsUvv/zCnDlzGnXDIqH+iOQsVBMSEsKqVas4dOgQPXr04OmnnyYiIoINGzbgcNTeyUu4dXa7nbVr19K9e3eef/55BgwYwM8//8yyZcsICAiQOzyhAYnkLPyufv368d1337Ft2zZUKhWTJk3i7rvvZuvWreKkYT1zOBysX7+eyMhIpk2bhsFgYNeuXezcuZPIyEi5wxNkIJKzcFMKhYLRo0dz7Ngx1qxZQ3FxMQ8//DD9+/dn06ZNYiR9m+x2O1988QV9+vRh8uTJ5RUZR48eZdiwYXKHJ8hIJGehTlQqFdOnT+fUqVN8+umn5OfnExcXR8+ePVm9erVYafgHmc1mVqxYQdeuXZk6dSpWq5XPP/+cY8eOMWnSJNHiVRDJWfhjNBoNjz/+OKdPn2bdunW4ubkxc+ZMwsLCWLBgAVlZWXKH2KhlZmby+uuvExoayuzZs/Hz82PTpk2cOHGCadOmiZN9QjmRnIVbolareeSRR/jvf//Lzp076dOnD2+88QahoaFMnz6dffv2iXlpF4fDwZ49e3jkkUcICwtj0aJFDBw4kG+//ZaffvqJ8ePHi5GyUI14RQi3RaFQMHz4cHbs2MHp06d54okn2Lp1K4MHD6Zbt24sXryYK1euyB2mLC5dusSiRYvo3Lkz0dHR7Nq1i7lz53L27Fk2b97Mgw8+KNvmoULjJ5KzUG+6du3KRx99RGZmJqtXryYwMJCXXnqJdu3a8dBDD7Fy5Upyc3PlDvOOunHjBsuWLeOBBx6gffv2/PWvfyU0NJS1a9eSmZlJQkIC4eHhcocpNAEiOQv1zsPDgxkzZvD9999z5swZ3njjDTIyMpg1axZBQUEMHTqUDz/8kEuXLskdar04d+4c//znP4mKiiIkJIQ5c+aQm5vLokWLOH/+PN999x2PPvooOp1O7lCFJkThrMPE4L59+1i0aBEOh4NJkyYxe/bs8tsyMjIYOnQoe/bsoW3btnc0WKHpcjqdHDlyhMTERBITEzl16hQgjbaHDx9OTEwMgwYNwtvbW+ZIa5eXl8f+/ftJTk4mOTmZc+fOAdCrVy/Gjx/PhAkTiIyMFFMWwk3VljtrTc52u53hw4ezatUqgoODmThxIgkJCXTq1KlOTyAINTlz5gw7duwgOTmZvXv3YjabUSgUREZG8sADD3Dvvfdy991306VLF1krGEpLSzlz5gxHjhzhxx9/ZP/+/Rw/fhwAd3d3HnzwQYYPH86oUaPo2LGjbHEKTU9tubPW3bfT0tIICwujXbt2AMTGxrJnz57y5CwIt6Jr16507dqVefPmYTabOXjwIPv37+f7779n1apVfPTRR4A0RRIZGUn37t3p1q0b3bp1o0OHDoSGhmIwGOotnoKCAtLT07lw4QKnTp3i9OnTnDp1irS0NEwmEwBeXl4MHDiQKVOmlB9A3NzqsM2yINyCWpNzVlYWISEh5V8HBweTlpZW/rXdbgfg2rVrdyA8oaXo0qULXbp04fHHH8dut3Pu3DmOHTvG8ePHOXXqFDt27GDNmjVV7mMwGAgODsbX1xc/Pz98fX3R6/Xll8ojbrvdjslkwmQyYTQaycvLIy8vj5ycHK5fv15to4GgoCA6duzI9OnT6dWrFxEREYSHh1cpebtx48ad/aMIzVpZzizLob9Va3Kuadaj8lxa2Qs0Pj7+lgIUhLowGAw1jpTtdjvZ2dlkZ2ff8mMHBgYSGBhY7ftZWVlkZWWRkpJyy48tCLW5ceMGYWFh1b5fa3IOCQmpMirOysoiKCio/OuIiAjWrl1LYGCgWN0kCIJQR3a7nRs3bhAREVHj7bUm5169enHx4kUuX75McHAwX3/9Ne+991757Tqdjn79+tVfxIIgCC1ETSPmMrUmZ7Vazd/+9jdmzZqF3W4nLi6Ozp0712uAgiAIQlV1qnNuit59912+++47NBoNoaGh/OMf/6jXs/tNRVJSEh999BHnzp1j/fr19OrVS+6QGszN6vNbildeeYWUlBT8/f3Zvn273OHI4urVq7z44otkZ2ejVCqZPHkyM2bMkDus2jmbqf379zttNpvT6XQ6Fy9e7Fy8eLHMEcnj7NmzznPnzjmnTZvmTEtLkzucBlNaWuocOnSoMz093WmxWJxjxoxx/vrrr3KH1eBSU1Odx48fd8bGxsodimyysrKcx48fdzqdTmdRUZEzJiamSbwWmu3y7UGDBqFWS7M2d911V4st9evYsWOL7OVQuT5fq9WW1+e3NP37928Sqy7vpKCgIHr27AmAp6cn4eHhTaK1bbNNzpVt3LiRqKgoucMQGlBN9flN4Q0p3FkZGRmcOnWK3r17yx1KrWo9IdiYPfbYYzXWtz733HNER0cD8Mknn6BSqRg7dmxDh9dg6vJ3aGmctdTnCy1PSUkJzzzzDK+++iqenp5yh1OrJp2cV69e+BMMqQAAASNJREFUfdPbExMTSUlJYfXq1c36jVnb36Elqq0+X2hZbDYbzzzzDGPGjCEmJkbucOqk2U5r7Nu3jxUrVvDJJ5+g1+vlDkdoYJXr861WK19//TUPPfSQ3GEJMnA6nbz22muEh4czc+ZMucOps2ZbSjds2DCsVis+Pj4A9O7dmwULFsgcVcPbvXs3CxcuJDc3F4PBQPfu3Vm5cqXcYTWIvXv38vbbb5fX58+ZM0fukBrc/PnzSU1NJS8vD39/f+bOncukSZPkDqtBHT58mPj4eLp06VLeG2X+/PkMHjxY5shurtkmZ0EQhKas2U5rCIIgNGUiOQuCIDRCIjkLgiA0QiI5C4IgNEIiOQuCIDRCIjkLgiA0QiI5C4IgNEIiOQuCIDRC/x9Wm2ce0nZsXQAAAABJRU5ErkJggg==
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
<p>There are a lot of built in plots, mostly for discrete data points and statistics. I mostly use the color palettes and things like that, but if you need to do statistical plots, look no further</p>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[34]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">Cols</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Rain&#39;</span><span class="p">,</span> <span class="s1">&#39;Temperature&#39;</span><span class="p">,</span> <span class="s1">&#39;Wind&#39;</span><span class="p">]</span>
<span class="n">N</span> <span class="o">=</span> <span class="mi">100</span>
<span class="n">Dates</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">date_range</span><span class="p">(</span><span class="s1">&#39;20161020&#39;</span><span class="p">,</span> <span class="n">periods</span><span class="o">=</span><span class="n">N</span><span class="p">)</span>
<span class="kn">from</span> <span class="nn">scipy.signal</span> <span class="kn">import</span> <span class="n">gaussian</span>
<span class="n">rain</span> <span class="o">=</span> <span class="n">gaussian</span><span class="p">(</span><span class="n">N</span><span class="p">,</span> <span class="mi">20</span><span class="p">)</span>
<span class="n">Temp</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mf">6.28</span><span class="p">,</span> <span class="n">N</span><span class="p">))</span>
<span class="n">Wind</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">N</span><span class="p">))</span> <span class="o">*</span> <span class="mf">0.3</span>
<span class="n">data</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">N</span><span class="p">,</span><span class="mi">3</span><span class="p">))</span>
<span class="n">data</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="n">rain</span>
<span class="n">data</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="n">Temp</span>
<span class="n">data</span><span class="p">[:,</span> <span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="n">Wind</span>
<span class="n">df2</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">index</span><span class="o">=</span><span class="n">Dates</span><span class="p">,</span> <span class="n">columns</span><span class="o">=</span><span class="n">Cols</span><span class="p">)</span>
<span class="n">df2</span><span class="o">.</span><span class="n">plot</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylim</span><span class="p">(</span><span class="o">-</span><span class="mf">1.1</span><span class="p">,</span> <span class="mf">1.1</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
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
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">sns</span><span class="o">.</span><span class="n">jointplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;Rain&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;Wind&#39;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">df2</span><span class="p">)</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt output_prompt">Out[35]:</div>
<div class="output_text output_subarea output_execute_result">
<pre>&lt;seaborn.axisgrid.JointGrid at 0x7f67ddffb320&gt;</pre>
</div>
</div>
<div class="output_area">
    <div class="prompt"></div>
<div class="output_png output_subarea ">
<img src="data:image/png;base64,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tW3bVg888IC6detmd9FbLJDXOmPGDM2cOVPLly9XRESE5s2bZ1xlU5L+4z/+Q++++66++uorDR8+XD//+c91+vRpSdKkSZOUkpKit956S+np6YqKitJjjz1mc4ndg22nAADGMrI7EQAAiRADABiMEAMAGIsQAwAYixADABiLEAO+ddlllyk7O1ujR4/WvffeG9AuGRMnTrSgZAAawxR74FvJycnasWOHJOnBBx9U3759dd9999lcKgBNMXKxMxBuQ4YM0SeffCLp7JZXP/nJT/T111/r9OnTys/P14gRIyR9F3zbt2/XU089pW7dumnPnj0aNGiQFi5caOTCXcAkhBhwnurqam3btk3jx4+XJHXo0EG/+93v1KlTJx0+fFi33nqr0tLS6gXU7t27VVRUpJiYGE2aNEkffPCBrrnmGjteAuAZhBjwrX/961/Kzs5WWVmZBg0apGHDhkk6uwP5r3/9a7333ntq06aNfD6fDh06pJ49e9b5+SuuuKLmdhsDBw5UWVkZIQaEGRM7gG9dcMEFWrt2rf77v/9bp06d0osvvihJWrdunQ4fPqzVq1dr7dq1uuiii3Ty5Ml6P1/7DgJt27ZVdXW1ZWUHvIoQA87TuXNnzZw5U88995xOnTqlo0ePqkePHmrXrp3+93//V2VlZXYXEcC3CDGgAZdffrkGDhyooqIiZWVladeuXRo7dqzWrVunSy65xO7iAfgWU+wBAMaiJQYAMBYhBgAwFiEGADAWIQYAMBYhBgAwFiEGADAWIQYAMNb/A93sYUD5A+d/AAAAAElFTkSuQmCC
"
>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[38]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span><span class="n">cols</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Abs&#39;</span><span class="p">,</span> <span class="s1">&#39;Conc&#39;</span><span class="p">,</span> <span class="s1">&#39;Molecule&#39;</span><span class="p">,</span> <span class="s1">&#39;Temp&#39;</span><span class="p">]</span>
<span class="n">Temps</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">25</span><span class="p">,</span> <span class="mi">50</span><span class="p">,</span> <span class="mi">75</span><span class="p">]</span>
<span class="n">Molecules</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Blue Dye&#39;</span><span class="p">,</span> <span class="s1">&#39;Orange Dye&#39;</span><span class="p">]</span>
<span class="n">Absorptivity</span> <span class="o">=</span> <span class="p">[</span><span class="mf">0.2</span><span class="p">,</span> <span class="mf">0.1</span><span class="p">]</span>   <span class="c1"># whatever units makes this reasonable</span>
<span class="n">Concs</span> <span class="o">=</span> <span class="p">[</span><span class="mf">0.1</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">,</span> <span class="mf">0.8</span><span class="p">,</span> <span class="mf">1.2</span><span class="p">]</span>
<span class="n">data</span> <span class="o">=</span> <span class="p">[]</span>
<span class="k">for</span> <span class="n">temp</span> <span class="ow">in</span> <span class="n">Temps</span><span class="p">:</span>
    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">Molecules</span><span class="p">)):</span>
        <span class="k">for</span> <span class="n">conc</span> <span class="ow">in</span> <span class="n">Concs</span><span class="p">:</span>
            <span class="n">A</span> <span class="o">=</span> <span class="n">Absorptivity</span><span class="p">[</span><span class="n">j</span><span class="p">]</span> <span class="o">*</span> <span class="n">conc</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">((</span><span class="mi">273</span> <span class="o">+</span> <span class="n">temp</span><span class="p">)</span> <span class="o">/</span> <span class="mi">300</span><span class="p">)</span>
            <span class="n">A</span> <span class="o">+=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">rand</span><span class="p">()</span> <span class="o">*</span> <span class="mf">0.05</span>
            <span class="n">data</span><span class="o">.</span><span class="n">append</span><span class="p">([</span><span class="n">A</span><span class="p">,</span> <span class="n">conc</span><span class="p">,</span> <span class="n">Molecules</span><span class="p">[</span><span class="n">j</span><span class="p">],</span> <span class="n">temp</span><span class="p">])</span>
<span class="n">AbsDF</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">columns</span><span class="o">=</span><span class="n">cols</span><span class="p">)</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">5</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">sns</span><span class="o">.</span><span class="n">lmplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;Conc&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;Abs&#39;</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s1">&#39;Molecule&#39;</span><span class="p">,</span>
           <span class="n">col</span><span class="o">=</span><span class="s1">&#39;Temp&#39;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">AbsDF</span><span class="p">,</span> <span class="n">col_wrap</span><span class="o">=</span><span class="mi">2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>
    </div>
</div>
</div>
<div class="output_wrapper">
<div class="output">
<div class="output_area">
    <div class="prompt"></div>
<div class="output_text output_subarea ">
<pre>&lt;matplotlib.figure.Figure at 0x7f67d947c198&gt;</pre>
</div>
</div>
<div class="output_area">
    <div class="prompt"></div>
<div class="output_png output_subarea ">
<img src="data:image/png;base64,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rIkjnlrx2uyh2SUqehcREREROVwxnYMyfvx4xo8fH3HszjvvbPlzQkICTz755GG/rgULGckOUpxxVGviTApNek/u7pWIiIiIiPRYPWaSfLMEh42sJCf2eMiaWK2QkG5OerfFUbAkIiIiItJD9ZgAxYKFzGRnfGRN7AmhovdU1ZWIiIiIiERRjwlQclITujc4aS56d6WbAYqIiIiIiERdjwlQbN21pcvmMLdwJaSbW7pERERERCRmekyAckRZLOBoLnpP6u7ViIiIiIgcNRSgtGa1hQcq2vRXIyIiIiJypOlbOIDDFcqWpKjoXURERESkGx29AYrFEh6oaHd292pERERERISjMUCxO0PZklQVvYuIiIiIxJmjI0CxWMwJ7650cCR292pEREREROQAeneA0lz07ko3/ywiIiIiInGtdwYojsRQN66U7l6JiIiIiIgcht4ToFitZtF7QpqK3kVEREREeqieH6DYE0KT3tPUIlhEREREpIfrmQGKxWLOLHGlmzNMRERERESkV+hZAYrNHp70rqJ3EREREZFep+cEKCl9IXNQd69CRERERERiqOdMKtT8EhERERGRXq/nBCgiIiIiItLrKUAREREREZG4oQBFRERERETihgIUERERERGJGwpQREREREQkbihAERERERGRuKEARURERERE4oYCFBERERERiRsKUEREREREJG4oQBERERERkbihAEVEREREROKGAhQREREREYkb9u5ewKEEAgEAysvLu3klIiLxIy8vD7v94JdwXT9FRNrqyPVTulfc/9vZs2cPANdcc003r0REJH4sXryYAQMGHPQxun6KiLTVketnrBx77LFccsklPPLIIwD4/X7Gjh3LyJEjef755w/4vDlz5rBmzRqmT58etbXMmDGDpKQkbrzxxqi9ZrTEfYBy4okn8sorr5CTk4PNZuvu5YiIxIW8vLxDPkbXTxGRtjpy/YyVpKQkNm7cSFNTEy6Xi48//pjc3NxuW0+8ivsAxeVycdppp3X3MkREehxdP0VE4s+4ceNYunQp559/PvPnz+eiiy5i1apVANTU1HDPPfdQVlZGYmIiDzzwAMcdd1zE86uqqvjtb3/Lzp07Abjnnns49dRTaWho4A9/+ANr1qwBYNq0aXzve99j1KhRfPnllwC89957LF26lIceeijiNbdt28b9999PdXU1LpeL3//+9xQWFsb6r+KAVCQvIiIiInKEXHjhhbz77rt4PB6+/fZbRo4c2XJuxowZHH/88cydO5ef//zn3H333W2e/+CDD3Ldddcxe/ZsZsyYwb333gvAM888Q0pKCnPnzmXu3LmMHj26w2u67777uO+++5gzZw533303999/f9d/0S6I+wyKiIiIiEhvcdxxx7F9+3bmzZvH+PHjI86tWrWKGTNmADBmzBhqamqoq6uLeMyKFSsoKSlp+bm+vp76+no++eQTHn300Zbj6enpHVpPQ0MDX375JXfeeWfLMa/Xe9i/VzQpQBEREREROYKKi4v585//zMsvv0xNTU3LccMw2jzWYrFE/BwMBvnnP/+Jy+WKOG4YRpvH7s/j8bQ5ZhgGaWlpvP3224fzK8SUtniJiIiIiBxBV155JbfddhvHHntsxPHTTz+dd955B4BPP/2UzMxMUlJSIh4zduxYZs2a1fLz+vXrATj77LMjju/btw+APn36UFpaSjAYZNGiRW3WkpKSwoABA1iwYAFgBiwbNmyIwm/ZeQpQRERERESOoLy8PK677ro2x6dNm8aaNWuYPHkyf/3rX9sUswP8z//8T8tjLrzwQl599VUAbr31Vmpra7n44ou55JJL+PTTTwH45S9/yc0338x1111HTk5Ou+t55JFHeOONN7jkkku46KKL2g1kjiSL0V4uSUREREREpBsogyIiIiIiInFDAYqIiIiIiMQNBSgiIiIiIhI31GZYerTq6mquv/56APbu3YvVaiUrKwuA119/HafT2Y2ri7RixQpuv/12BgwYAMD555/PrbfeCsCyZcv44x//SDAY5Pvf/z433XRTdy5VRI4CPen6+cILLzB//nwA/H4/mzdv5tNPPyU1NZVx48aRnp6O1WrF6XTy+uuvd/NqRaSrVCQvvcaMGTNISkrixhtv7O6ltGvFihXMmjWLZ555JuK4z+fj/PPP5+WXXyYnJ4cpU6bw5JNPMnjw4G5aqYgcbeL9+tnawoULefXVV/n73/8OwLhx45g3bx5paWndvDIRiRZlUKTXevPNN3nllVfw+XyMGjWK6dOnEwwGGT16NFOnTmXlypVkZWVxxx138Mgjj7Br1y6mT5/O+PHjef3111m6dClNTU1s376dSy+9lNtuuy0m6/z6668pLCykf//+gJlZWbx4sbIoItJt4vn6OW/ePC66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aVZXV0d2djYOh4OVK1eyY8eOg75+eno6ycnJfPXVVwC8++67LefGjh3Lq6++is/nA8wtWofahlVVVcVvf/tbrrnmmpYMz9SpU/nDH/7AiBEjWjI9Y8eOZdasWS0B0rp16zry16EMioiIiIhIh511p1lz4sXMnPjcEPSaxzvJYrHw9NNPc//99/PMM88QDAYZP348v/jFL9p9/OTJk7n11lu54oorGD58eIcyFA8++CD33nsvSUlJnHHGGaSkpABmYLFjxw6uuOIKDMMgMzOTZ555ps3zm5qauPTSS1vaDF966aX8+Mc/bjl/4oknkpKS0rK9C+C2227jj3/8I5dccgmGYdC/f3+ef/75Q/99GAfL+cSB7du3M2nSJBYvXsyAAQO6ezkiIj2Grp8iIjHy3UKz5qRmm5k5OevOTtefHCkNDQ0kJycD8MILL7B7927uvffeqL1+RUUF1157LQsWLOjybBRlUEREREREDsew8+I+INnfsmXLeP755wkEAhxzzDE89NBDUXvtt956i8cee4xf//rXURncqABFRERERHq1YNBgT72H3DRXdy+l21x44YVceOGFMXntyy67jMsuuyxqr6cARURERER6La8/SEVtE75AsLuXIh2kAEVEREREeqVGr5/dtR6C8V1yLftRgCIiIiIivU51g5fqRm93L0M6QXNQRERERKTXCAYNKmqbIoKTBo+fB+ev78ZVyeFQBkVEREREeoX26k027annd3PXsb3afZBnSjxRgCIiIiIiPV6Dx8+eush6kw/WVfDYwu/w+IM4bJZuXJ0cDgUoIiIiItKj7V9v4vUHefrDEuau3gVAXloCT1w1qruWJ4dJAYqIiIiI9EjBoMHuOg+NXn/LsfJ9Tfxu7lq+q6gHYExhNjOuOpk+qUfvDJSeRgGKiIiIiPQ47dWbrNxUyZ8WbKCuyY/VArdOKOIX5w7FZlNfqJ5EAYqIiIiI9Cj715sEggYvrtjCK59uAyAjycGjU0+meHjf7lymdJICFBERERHpMaoavNS0qjepbvTy4Pz1fLGtBoAR/dN59ppTGJCV1F1LlC5SgCIiIiIica+9epM1O/bxwLx17K03A5Zrzizgd5ecgENbuno0BSgiIiIiEtf2rzcxDIPZX+zg+eWbCAQNEh02/nTFCC4b1b+bVyrRoABFREREROLW/vUmDR4/f/ngO5Z9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xbh0CzQqcVrcpd6EiIgoQgzrAEWrViHVwps0EcW2aTnxeHz59bDotdBr1UiP00PN02IiIopQwzZAMcoapFp0vEkTUcx76LbxsOi1iDNokWxivQkREUW2YRegSJKERKMWCUY53EshIhoSKpUKKRYd602IiCgqDKsAhXnXRDQcpTE4ISKiKDJsAhSmdBHRcKXTBH+YLRERUagMiwAl0Sgj0cSULiIiIiKiSBfSx2q7d+/GvHnzUFxcjJdffrnH6y6XCz/84Q9RXFyMu+66C2fPng3q99eoVMiMNzA4ISIiIiKKEiELULxeL37xi19g48aNKCkpwdatW3H8+PEu7/nb3/6GuLg4fPjhh/jOd76DZ599Nmjf3yCrMSJBD4PMehMiIiIiomgRsgClrKwMubm5yM7OhizLWLRoEUpLS7u8Z8eOHbjjjjsAAPPmzcPevXuhKMpVf+9Eo4zMeAM0auZdExERERFFk5D9BF9bW4uMjIz2f09PT0dtbW2P92RmZgIANBoNLBYLGhoaBv091SqJKV1ERERERFEsZEXyvZ2EdB8OFsh7AqXXqpFm0fHUhIiIiIgoioXsp/mMjAzU1NS0/3ttbS3S0tJ6vOfChQsAAI/Hg5aWFiQkJAz4eyUYZYxIYEoXEREREVG0C9lP9Pn5+aiqqkJ1dTVcLhdKSkpQWFjY5T2FhYV4++23AQDbt2/HzJkzB3SColZJyIjXI4kpXUREREREMSFkKV4ajQZr1qzBypUr4fV6sWzZMuTl5WHDhg2YPHkyioqKcOedd+Lhhx9GcXEx4uPj8fzzzwf8+TqtGulM6SIiIiIiiikhHdRYUFCAgoKCLl9btWpV+691Oh1+85vfDPhz4w1aJJnkQderEBERERFRZIqqSfIqSUKqRQeTLqqWTUREREREAYqan/RljQojEw3QMqWLiIiIiChmRc1P+2kWHYMTIiIiIqIYFzU/8bPehIiIiIgo9kVNgEJERERERLGPAQoREREREUUMBihERERERBQxGKAQEREREVHEYIBCREREREQRgwEKERERERFFDAYoREREREQUMRigEBERERFRxGCAQkREREREEYMBChERERERRQwGKEREREREFDEYoBARERERUcRggEJERERERBGDAQoREREREUUMBihERERERBQxGKAQEREREVHEYIBCREREREQRgwEKERERERFF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
"
>
</div>
</div>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight highlight-ipynb hl-python"><pre><span></span>
</pre></div>
    </div>
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