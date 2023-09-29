# Create a Custom Font Theme for Office on a Mac Using XML

## Overview

This guide walks you through creating a custom font theme for Microsoft Office on a Mac. You'll use XML to define your fonts and will specifically use "Roboto" for headings and "Open Sans" for body text.

## Decide on Fonts

First, download and install the fonts you want to use. For this example, download "Roboto" for headings and "Open Sans" for body text from [Google Fonts](https://fonts.google.com/).

## Make Hidden Files Visible

1. Hold down the **Option** key.
2. Open the **Go** menu.
3. Select **Library**.

## Navigate to the Office Theme Folder

Go to `Users/YourUserName/Library/Group Containers/UBF8T346G9.Office/User Content/Themes`.

## Create the XML File

1. Open a text editor like `TextEdit`.
2. Copy and paste the following XML code to define your fonts:

    ```xml
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <a:fontScheme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="GoogleFontsTheme">
      <a:majorFont>
        <a:latin typeface="Roboto"/>
        <a:ea typeface=""/>
        <a:cs typeface=""/>
      </a:majorFont>
      <a:minorFont>
        <a:latin typeface="Open Sans"/>
        <a:ea typeface=""/>
        <a:cs typeface=""/>
      </a:minorFont>
    </a:fontScheme>
    ```

3. Save the file with an `.xml` extension inside the `Themes` folder you located earlier.

## Apply the Custom Font Theme

1. Open an Office application like Word or PowerPoint.
2. Navigate to the **Design** tab.
3. In the **Font Themes** dropdown, select your custom font theme.

## Test the Theme

Open a new document or an existing one to confirm that your custom font theme applies correctly.

## Troubleshoot

- If the theme doesn't appear, restart the Office application and try again.
- Double-check the XML file to make sure it's correctly formatted.
