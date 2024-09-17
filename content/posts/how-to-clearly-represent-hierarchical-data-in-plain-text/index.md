---
title: How to Clearly Represent Hierarchical Data in Plain Text
date: 2024-09-17T21:03:00.515Z
---
S﻿ometimes You end up writing on a Library computer. Logged into a plain text editor and you need to represent some data but indentation isnt an option as the web editor your working with jumps you to the submit button. Can't use org tables/vimwiki tables because you don't have access to your editor with your custom vimrc and plugins to auto format pipes into nice human readable tables. What to do?

M﻿ethod 1: Custom Delimiters

U﻿sing a custom delimiter for diferent levels

```
Level1 Name
- Level2 Property1: Value1
- Level2 Property2: Value2
-- Level3 Property1: Value1
-- Level3 Property2: Value2
Level1 Another Name
- Level2 Property1: Value1
```

M﻿ethod 2:  Using Symbols For Different Levels

```
* Level1: Name
  - Level2: Sublevel1
    + Property1: Value1
    + Property2: Value2
  - Level2: Sublevel2
    + Property1: Value1
* Level1: Another Name
  - Property1: Value1
```

###  Pros And Cons

| **Aspect** | **Custom Delimiters**                                                                                                                                                                                                                                 | **Symbols**                                                                                                                                                                                                                                                                        |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Pros**   | \- Clarity and Precision: Tailored to fit specific needs. <br> - Consistency: Well-defined system reduces ambiguity. <br> - Flexibility: Can be customized for unique data formats. <br> - Readability: Descriptive delimiters enhance understanding. | \- Simplicity: Easy to recognize and understand. <br> - Readability: Clear visual representation of hierarchy. <br> - Ease of Use: Familiar to many users for lists and hierarchies. <br> - Visual Structure: Immediate hierarchy visualization.                                   |
| **Cons**   | \- Complexity: Overly complex delimiters can create confusion. <br> - Maintenance: Requires additional documentation and adjustments. <br> - Ambiguity: Potential overlap with data content.                                                          | \- Limited Depth: Might struggle with very deep hierarchies. <br> - Inconsistency: Varying interpretations of symbols. <br> - Interpretation Variability: Different people might interpret symbols differently. <br> - Lack of Precision: Less descriptive than custom delimiters. |