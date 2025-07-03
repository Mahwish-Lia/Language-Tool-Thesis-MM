<!--
author:    Masub.Makhdoom
email:     masub.makhdoom@ovgu.de
version:   0.0.1
language:  en
narrator:  US English Female
comment:   Template for SpeechRecognition-powered quizzes in LiaScript
logo:      logo.jpg

@SpeechRecognition.support
<script modify="false" run-once>
// Vendor prefix
const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
if (!SpeechRecognition) {
  "LIASCRIPT: > 'Speech Recognition' not supported in this browser. Try Chrome, Opera, or Edge.";
} else {
  "LIASCRIPT: > Your browser does support 'Speech Recognition' ..."
}
</script>
@end

@SpeechRecognition
<script>
// Vendor prefix
const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
if (!SpeechRecognition) {
  alert('SpeechRecognition not supported. Try Chrome, Opera, or Edge.');
} else {
  const recognition = new SpeechRecognition();
  recognition.lang = '@0';
  recognition.interimResults = false;
  recognition.continuous = false;

  const solution = "@1".toLowerCase()
    .replace(/(\.|\?|\!|\,|\-|\;)/g," ")
    .replace(/[ ]+/g," ")
    .trim();

  recognition.onresult = ev => {
    let t = ev.results[0][0].transcript?.toLowerCase().trim() || '';
    if (t === solution) {
      send.lia("true");
    } else {
      send.lia("Please try again …",[],false);
    }
  };
  recognition.onerror = ev => send.lia("Error: "+ev.error,[],false);
  recognition.onend   = () => console.log('Speech recognition ended.');
  recognition.start();
}
"LIA: wait"
</script>
@end



@SpeechRecognition.withFeedback
<script>
// Vendor prefix
const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
if (!SpeechRecognition) {
  alert('SpeechRecognition not supported. Try Chrome, Opera, or Edge.');
} else {
  const recognition = new SpeechRecognition();
  recognition.lang = '@0';
  recognition.interimResults = false;
  recognition.continuous = false;

  const solution = "@1".toLowerCase()
    .replace(/(\.|\?|\!|\,|\-|\;)/g," ")
    .replace(/[ ]+/g," ")
    .trim();

  recognition.onresult = ev => {
    let t = ev.results[0][0].transcript?.toLowerCase().trim() || '';
    if (t === solution) {
      send.lia("true");
    } else {
      send.lia(t,[],false);
    }
  };
  recognition.onerror = ev => send.lia("Error: "+ev.error,[],false);
  recognition.onend   = () => console.log('Speech recognition ended.');
  recognition.start();
}
"LIA: wait"
</script>
@end
-->

<!--
author: Your Name
version: 1.0
language: en
comment: PowerPoint-style LiaScript presentation template
-->

<!--
author: Your Name
version: 1.0
language: en
comment: Civic PowerPoint Theme Clone in LiaScript
-->

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Title Page
</span>

<svg xmlns='http://www.w3.org/2000/svg' width='800' height='450' viewBox='0 0 800 450'>
  <!-- Background -->
  <rect width='800' height='450' fill='#1A237E' />
  
  <!-- White rounded rectangle container -->
  <rect x='50' y='50' width='700' height='350' rx='20' fill='white' />
  
  <!-- Title -->
  <text x='400' y='130' font-family='Segoe UI, Arial, sans-serif' font-size='50' font-weight='bold' text-anchor='middle' fill='#1A237E'>
    ARTIFICIAL INTELLIGENCE
  </text>
  
  <!-- Subtitle -->
  <text x='400' y='200' font-family='Segoe UI, Arial, sans-serif' font-size='90' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    CONFERENCE
  </text>
  
  <!-- Level / Year (removed UNESCO & OVGU text) -->
  <!--
  <text x='400' y='270' font-family='Segoe UI, Arial, sans-serif' font-size='40' font-weight='bold' text-anchor='middle' fill='#1A237E'>
      UNESCO & OVGU
  </text>
  -->
  
  <!-- Footer -->
  <text x='400' y='320' font-family='Segoe UI, Arial, sans-serif' font-size='22' text-anchor='middle' fill='gray'>
    Powered by LiaScript
  </text>
</svg>

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

  <div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
    <!-- Optional caption -->
  </div>

</div>





## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Title 
</span>

> content
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>


<style>
section {
  background-color: #f5f7fa;
  padding: 2em;
  border-radius: 20px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}
h1, h2, h3 {
  color: #4a90e2;
}
</style>

---


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Goals
</span>

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>


>* 1
>* 2 
>* 3 
>* 4
>* 5

---

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Heading
</span>
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

  <div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
    <!-- You can add caption or description here -->
  </div>

</div>
---

<div style="background: linear-gradient(to right, #1e3c72 0%, #2a5298 100%);
            padding: 2em; border-radius: 20px; color: #e0e7ff;">
  
###  Stylish Gradient Section

You can write there what you want

</div>


---

<div style="background: rgba(74,144,226,0.1);
            border: 1px solid #4a90e2;
            backdrop-filter: blur(8px);
            padding: 2em;
            border-radius: 20px;
            color: #0d2d57;">

###  Cool Blue Glass Effect

Modern "glassmorphism" design with soft blur and blue tones.


</div>


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 4
</span>
<div style="background: linear-gradient(to right, #d0eaff, #f0faff);
            padding: 2em;
            border-radius: 20px;
            color: #2e4d1b;
            font-weight: bold;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);">

###  Calm and Fresh

Inspired by nature — great for eco, calm, or relaxing themes.

</div>


<div style="background: linear-gradient(to right, #6a11cb, #2575fc);
            padding: 2em;
            border-radius: 20px;
            color: #ffffff;
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.2);">

###  Vibrant Neon Slide

Bright text on a neon-style background — great for modern tech.

</div>
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

<img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 5
</span>
<div style="display: flex; gap: 2em; justify-content: space-between;">

 <div style="flex: 1;
             background: linear-gradient(to bottom, #1e3c72, #2a5298);
             padding: 1.5em;
             border-radius: 15px;
             box-shadow: 0 0 10px rgba(0,0,0,0.1); 
             color: #ffffff;">
             
  ### ✅ Option A

  - Simple  
  - Classic look   
  - Dark blue theme
  
</div>



  <div style="flex: 1;
              background: linear-gradient(to bottom, #c2e9fb, #a1c4fd);
              padding: 1.5em;
              border-radius: 15px;
              box-shadow: 0 0 10px rgba(0,0,0,0.1);
              color: #333;">
              
  ### 🚀 Option B

  - Modern
  - Tech style
  - Cool tones

  </div>

</div>
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

<img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 6 
</span>
<div style="flex: 1;
            background: linear-gradient(to bottom right, #cce0f5, #e6f0fa);
            padding: 1.5em;
            border-left: 8px solid #5b9bd5;
            border-radius: 15px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            color: #2b3f54; font-weight: bold;">

### 💙 Elegant Look  
- Soft blue hues  
- Feels modern and clean  
- Good for soft content

</div>

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

 <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 7 
</span>
<div style="flex: 1;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255,255,255,0.3);
            backdrop-filter: blur(10px);
            padding: 1.5em;
            border-radius: 20px;
            color: #004e92;
            font-weight: bold;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);">

###  Frosty Glass  
- Transparent style  
- High-tech modern feel  
- Try on dark background

</div>
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

<img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 8 
</span>

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="Logo" style="width: 100%; border-radius: 10px;" />

  <div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
    <!-- Optional caption here -->
  </div>

</div>

<div style="flex: 1;
            background: linear-gradient(to right, #a1c4fd, #c2e9fb);
            padding: 1.5em;
            border-radius: 20px;
            box-shadow: inset 0 0 5px #fff, 0 0 15px rgba(0,0,0,0.1);
            color: #1a3e72;
            font-weight: bold;">

  ### Fresh & Focused  
*   Light blue theme
 
*   Calm and soothing
 
*   Great for clarity and focus

</div>


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 9
</span>
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

  <div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
    <!-- You can add caption or description here -->
  </div>

</div>
<div style="display: flex; gap: 1.5em; justify-content: space-between;">

 <div style="flex: 1;
              background: #0b1d3a;
              padding: 1.5em;
              border-radius: 12px;
              color: #ffffff;
              font-weight: bold;
              box-shadow: 0 2px 6px rgba(0,0,0,0.3); 
              text-align: center;">

    ### 📘 Step 1  
    Introduction to Topic  
    (Light content)

</div>


  <div style="flex: 1;
              background: #ffffff;
              padding: 1.5em;
              border-radius: 12px;
              color: #004080;
              font-weight: bold;
              box-shadow: 0 2px 6px rgba(0,0,0,0.1);
              text-align: center;">

    ### 📗 Step 2  
    Core Concepts  
    (Main content)

  </div>

  <div style="flex: 1;
              background: #e6f2ff;
              padding: 1.5em;
              border-radius: 12px;
              color: #004080;
              font-weight: bold;
              box-shadow: 0 2px 6px rgba(0,0,0,0.1);
              text-align: center;">

    ### 📙 Step 3  
    Practice & Wrap-up  
    (Activity slide)

  </div>
  

</div>

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 10
</span>
 ## 📈 Progress Bar Graph Example

| Task          | Progress          |
|---------------|-------------------|
| Reading       | ██████████░░░░░░ 60%  |
| Writing       | ████████░░░░░░░░ 50%  |
| Speaking      | █████████████░░░ 75%  |
| Listening     | ███████████████░ 85%  |

<style>
table {
  width: 60%;
  border-collapse: collapse;
  margin: 1em 0;
}
th, td {
  border: 1px solid #b3d1ff;
  padding: 0.5em 1em;
  text-align: left;
  color: #004080;
}
th {
  background: #e6f2ff;
}
td:nth-child(2) {
  font-family: monospace;
}
</style>
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

<img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 11 
</span>
 ## 📋 Comparison Table

| Feature        | Traditional           | LiaScript             |
|----------------|-----------------------|-----------------------|
| Interactivity  | ❌ No                 | ✅ Yes                |
| Audio/Video    | ❌ No                 | ✅ Yes                |
| Quizzes        | Paper-based           | Embedded & auto-graded|
| Code Execution | ❌ No                 | ✅ Yes                |

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

<img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 12 
</span>
| Feature        | Traditional           | LiaScript             |
|----------------|-----------------------|-----------------------|
| Interactivity  | ❌ **No**             | ✅ **Yes**            |
| Audio/Video    | ❌ **No**             | ✅ **Yes**            |
| Quizzes        | Paper-based           | ✅ **Embedded & auto-graded** |
| Code Execution | ❌ **No**             | ✅ **Yes**            |


<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

 <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 13
</span>
<table style="border-collapse: collapse; width: 70%; color: #004080;">
  <thead>
    <tr style="background-color: #e6f2ff;">
      <th style="border: 1px solid #b3d1ff; padding: 0.5em;">Feature</th>
      <th style="border: 1px solid #b3d1ff; padding: 0.5em;">Traditional</th>
      <th style="border: 1px solid #b3d1ff; padding: 0.5em;">LiaScript</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Interactivity</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">No</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Yes</td>
    </tr>
    <tr>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Audio/Video</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">No</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Yes</td>
    </tr>
    <tr>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Quizzes</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Paper-based</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Embedded & auto-graded</td>
    </tr>
    <tr>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Code Execution</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">No</td>
      <td style="border: 1px solid #b3d1ff; padding: 0.5em;">Yes</td>
    </tr>
  </tbody>
</table>
<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

 <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 14 
</span>
 ## 🏆 Learning Progress

| Skill     | Progress        |
|-----------|-----------------|
| Grammar   | █████████░░░ 80% |
| Vocabulary| ███████░░░░░ 60% |
| Speaking  | ██████████░░░ 70% |
| Listening | ███████████░░ 85% |

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

 <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>


## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 15 
</span>

What is the official name of Germany?

- [( )] Federal Germany
- [(X)] Bundesrepublik Deutschland 

Germany has [[16]] states

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

 <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

<div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
  <!-- You can add caption or description here -->
</div>

  
</div>

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Slide 16
</span>

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

  <div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
    <!-- You can add caption or description here -->
  </div>

</div>

   {{0}}
Germany, officially known as the Federal Republic of Germany, is a country located in Central Europe. It shares borders with nine countries, including France, Poland, and Austria, making it an important hub for European culture and politics. Germany’s capital and largest city is Berlin, known for its rich history and vibrant cultural scene.

[https://www.youtube.com/watch?v=Q_4qEXbFOxY](https://)

   {{1}}
   With a population of approximately 83 million people, Germany is the most populous country in the European Union. The official language is German, and the country is divided into 16 federal states, each with its own government. Germany has a federal parliamentary republic system, which ensures a balance of power between the national and regional governments.
   [https://www.youtube.com/watch?v=3Pxmz4OLuZo](https://)

  {{2}}
  Germany is known for its strong economy, being the fourth-largest in the world by nominal GDP. It has a highly developed industrial base, famous for its automotive industry with brands like Volkswagen, BMW, and Mercedes-Benz. Besides manufacturing, Germany excels in engineering, technology, and exports, contributing significantly to the global market.

## <span style="color:#00008B; font-size:1.8em; font-weight:bold">
Text-to-Speech
</span>

<div style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0.8;
    z-index: 1000;
    text-align: center;
    width: 120px;
">

  <img src="https://github.com/Masub27/Intro/blob/main/ChatGPT%20Image%20Jul%203,%202025,%2012_53_14%20PM.png?raw=true" alt="UNESCO Logo" style="width: 100%; border-radius: 10px;" />

  <div style="font-size: 0.9em; color: #555; margin-top: 0.3em;">
    <!-- You can add caption or description here -->
  </div>

</div>

   --{{0}}--
   The country also has a rich cultural heritage with contributions to music, philosophy, literature, and science. Famous personalities such as Beethoven, Goethe, and Einstein hail from Germany. Additionally, Germany offers diverse landscapes from the Bavarian Alps in the south to the North Sea coast in the north, making it an attractive destination for tourists worldwide.












