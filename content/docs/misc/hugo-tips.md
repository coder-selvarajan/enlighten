# Hugo Syntax/Tips

### **Emoji**

Emojis can be enabled in hugo by adding below property in configuration file.
    
    enableEmoji = "true"

Emoji Cheat-sheat:
https://www.webpagefx.com/tools/emoji-cheat-sheet/
 
`SYNTAX:` remove space after first `:` 

    I : heart: Hugo!

`RESULT:`

I :heart: Hugo!

---

### **Task List**

`SYNTAX:`

    1. [ ] a task list item
    2. [x] list syntax required
    3. [ ] incomplete
    4. [x] completed

`RESULT:`

1. [ ] a task list item
2. [x] list syntax required
3. [ ] incomplete
4. [x] completed

---

### **Footnote**

`SYNTAX:`

    This is a footnote.[^1]
    [^1]: the footnote text.

`RESULT:`

This is a footnote.[^1]
[^1]: the footnote text.

---

### **Definition List**

`SYNTAX:`

    Cat
    : Fluffy animal everyone likes

    Internet
    : Vector of transmission for pictures of cats


`RESULT:`

Cat
: Fluffy animal everyone likes

Internet
: Vector of transmission for pictures of cats

---

### **Figure**

`SYNTAX:`

    {{ < figure src="../../images/hugo.png" title="Hugo" > }}

`RESULT:`

{{< figure src="../../../images/hugo.png" title="Hugo" >}}

---

### **Gist** (Github)

`SYNTAX:` 
    
    {{ < gist spf13 7896402 >}}

`RESULT:`

{{< gist spf13 7896402 >}}

---

### **Video (Youtube & Vimeo)**

#### **Youtube** video sample:

`SYNTAX:`

    {{ < youtube w7Ft2ymGmfc >}}

`RESULT:`

{{< youtube w7Ft2ymGmfc >}}


#### **Vimeo** video sample: 

`SYNTAX:`
    
    {{ < vimeo 146022717 >}}

`RESULT:`

{{< vimeo 146022717 >}}
