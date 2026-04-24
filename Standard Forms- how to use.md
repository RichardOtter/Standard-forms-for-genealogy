
The actual text that is pre-printed on a form is of the most interest,
however, other text that describes the form etc is also included.
These documents have been saved in XML format to make the distinctions clear.



The idea is that the abridged Data entry version is used to transcribe records 
where the full form was used.
The prompt for each data item on the original form is short but unambiguous. 
A transcription will have a copy of the abridged form along with the transcribed
data along with the XML header that specifies the form name and version.

This is a full template showing the XML elements

<FORM ID="F251124" REV="1" NAME="Bavarian Military Rosters WWI, Type=A">

<NOTES>
</NOTES>

<FORM_TEXT>
form text goes here
</FORM_TEXT>

<NOTES>
</NOTES>

===========================================DIV50==
<FORM_DATA>
data entry version of the form goes here
</FORM_DATA>
</FORM>


Each form has an ID. The ID should be unique.
The current format is YYMMDD of the date of creation.
Rule is that one ID is created per calendar day. One 

If the form is updated later, ther REV number is incremented.
The Name should be descriptive and also similar to the file name.

When creating a transcription, use this part of the full form file-

```xml
<FORM ID="F251124" REV="1" NAME="Bavarian Military Rosters WWI, Type=A">
<FORM_DATA>
data entry version of the form goes here
</FORM_DATA>
</FORM>
```

XML rules

there are 2 forbidden characters in text
< and & but they can be entered as &lt; and &amp;


For including text that is not actually in the form or in the
filled-out form, enclose the text in these special arrows-
 ► text ◄

```xml
  ►_       _◄       start and end of a blank space in a pre-printed form to be filled in by user.
<s> </s>           start and end of strike-out text. Usually pre-printed text not applicable.
                   start and end of text inserted by hand, but not in a blank.
<stamp> </stamp> start and end of text stamped either in a blank or elsewhere onto the document
<bk/>               a space on the form left blank
<sig> </sig>   start and end of a signature
```