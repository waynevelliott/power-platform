---
title: Lower, Upper, and Proper functions in Power Apps
description: Reference information including syntax and examples for the Lower, Upper, and Proper functions in Power Apps.
author: gregli-msft

ms.topic: reference
ms.custom: canvas
ms.reviewer: tapanm
ms.date: 11/07/2015
ms.subservice: power-fx
ms.author: gregli
search.audienceType:
  - maker
search.app:
  - PowerApps
contributors:
  - gregli-msft
  - tapanm-msft
---

# Lower, Upper, and Proper functions in Power Apps

Converts letters in a string of text to all lowercase, all uppercase, or proper case.

## Description

The **Lower**, **Upper**, and **Proper** functions convert the case of letters in strings.

- **Lower** converts any uppercase letters to lowercase.
- **Upper** converts any lowercase letters to uppercase.
- **Proper** converts the first letter in each word to uppercase if it's lowercase and converts any other uppercase letters to lowercase.

All three functions ignore characters that aren't letters.

If you pass a single string, the return value is the converted version of that string. If you pass a single-column [table](/power-apps/maker/canvas-apps/working-with-tables) that contains strings, the return value is a single-column table of converted strings. If you have a multi-column table, you can shape it into a single-column table, as [working with tables](/power-apps/maker/canvas-apps/working-with-tables) describes.

## Syntax

**Lower**( _String_ )<br>**Upper**( _String_ )<br>**Proper**( _String_ )

- _String_ - Required. The string to convert.

**Lower**( _SingleColumnTable_ )<br>**Upper**( _SingleColumnTable_ )<br>**Proper**( _SingleColumnTable_ )

- _SingleColumnTable_ - Required. A single-column table of strings to convert.

## Examples

### Single string

The examples in this section use a text-input control, named **Author**, as their [data source](/power-apps/maker/canvas-apps/working-with-data-sources). The control contains the string "E. E. CummINGS".

| Formula                             | Description                                                                                                                   | Result           |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ---------------- |
| **Lower(&nbsp;Author.Text&nbsp;)**  | Converts any uppercase letters in the string to lowercase.                                                                    | "e. e. cummings" |
| **Upper(&nbsp;Author.Text&nbsp;)**  | Converts any lowercase letters in the string to uppercase.                                                                    | "E. E. CUMMINGS" |
| **Proper(&nbsp;Author.Text&nbsp;)** | Converts the first letter of each word to uppercase if it's lowercase, and converts any other uppercase letters to lowercase. | "E. E. Cummings" |

### Single-column table

The examples in this section convert strings from the **Address** [column](/power-apps/maker/canvas-apps/working-with-tables#columns) of the **People** data source, which contains this data:

![Table example.](media/function-lower-upper-proper/people-table.png)

Each formula returns a single-column table that contains the converted strings.

| Formula                                                       | Description                                                                                                                     | Result                                                                |
| ------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **Lower( ShowColumns(&nbsp;People,&nbsp;"Address"&nbsp;) )**  | Converts any letter that's lowercase to uppercase.                                                                              | ![Lower.](media/function-lower-upper-proper/people-table-lower.png)   |
| **Upper( ShowColumns(&nbsp;People,&nbsp;"Address"&nbsp;) )**  | Converts any letter that's lowercase to uppercase.                                                                              | ![Upper.](media/function-lower-upper-proper/people-table-upper.png)   |
| **Proper( ShowColumns(&nbsp;People,&nbsp;"Address"&nbsp;) )** | Converts any first letter of a word that's lowercase to uppercase, and converts any other letter that's uppercase to lowercase. | ![Proper.](media/function-lower-upper-proper/people-table-proper.png) |

### Step-by-step example

1. Add a **[Text input](/power-apps/maker/canvas-apps/controls/control-text-input)** control, and name it **Source**.
2. Add a label, and set its **[Text](/power-apps/maker/canvas-apps/controls/properties-core)** property to this function:<br>**Proper(Source.Text)**
3. Press F5, and then type **WE ARE THE BEST!** into the **Source** box.<br>The label shows **We Are The Best!**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]