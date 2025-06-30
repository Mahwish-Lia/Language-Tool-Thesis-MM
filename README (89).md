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
# 1 Herzlich Willkommen
<!-- A1 German Course Cover -->
<svg xmlns='http://www.w3.org/2000/svg' width='800' height='450' viewBox='0 0 800 450'><rect width='800' height='450' fill='%23228B22'/><rect x='50' y='50' width='700' height='350' rx='20' fill='white'/><text x='400' y='150' font-family='Arial' font-size='60' font-weight='bold' text-anchor='middle' fill='%23228B22'>DEUTSCH</text><text x='400' y='240' font-family='Arial' font-size='100' font-weight='bold' text-anchor='middle' fill='green'>A1</text><text x='400' y='300' font-family='Arial' font-size='40' text-anchor='middle' fill='%23228B22'>Sprachkurs für Anfänger</text><text x='400' y='350' font-family='Arial' font-size='20' text-anchor='middle' fill='gray'>powered by LiaScript</text></svg>

# Hallo Deutschland!

 ## <span style="color:#006400;font-size:1.8em;font-weight:bold">
 Das Alphabet: Hören Sie die Buchstaben und sprechen Sie nach
</span>

?[](https://github.com/Masub27/Intro/blob/main/KursDaF_A1_KB_Track_001.mp3?raw=true)

<div style="
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.2;
    font-size: 8em;
    color: grey;
    z-index: 1000;
">
    Masub
</div>


 | Buchstabe | Lautschrift  | Beispielwort |
|-----------|-------------|--------------|
| A a       | [aː]        | Apfel        |
| B b       | [beː]       | Ball         |
| C c       | [tseː]      | Computer     |
| D d       | [deː]       | Dorf         |
| E e       | [eː]        | Elefant      |
| F f       | [ɛf]        | Fisch        |
| G g       | [geː]       | Garten       |
| H h       | [haː]       | Haus         |
| I i       | [iː]        | Igel         |
| J j       | [jɔt]       | Jagd         |
| K k       | [kaː]       | Kuchen       |
| L l       | [ɛl]        | Lampe        |
| M m       | [ɛm]        | Mond         |
| N n       | [ɛn]        | Nase         |
| O o       | [oː]        | Ostern       |
| P p       | [peː]       | Pferd        |
| Q q       | [kuː]       | Qualle       |
| R r       | [ɛʁ]        | Rose         |
| S s       | [ɛs]        | Sonne        |
| T t       | [teː]       | Tisch        |
| U u       | [uː]        | Uhr          |
| V v       | [faʊ]       | Vogel        |
| W w       | [veː]       | Wasser       |
| X x       | [ɪks]       | Xylophon     |
| Y y       | [ˈʏpsilɔn]  | Yoga         |
| Z z       | [tsɛt]      | Zebra        |
| Ä ä       | [ɛː]        | Äpfel        |
| Ö ö       | [øː]        | Öl           |
| Ü ü       | [yː]        | Übung        |
| ẞ ß       | [ɛsˈtsɛt]   | Straße       |



 
# Horen Sie und sprechen sie nach

?[](https://github.com/Masub27/Thesis-collection/blob/main/KursDaF_A1_KB_Track_002.mp3?raw=true)

L-e-i-p-z-i-g
![](https://github.com/Masub27/Thesis-collection/blob/main/Leipzig.webp?raw=true)

B-e-r-l-i-n
![](https://github.com/Masub27/Thesis-collection/blob/main/berlin.avif?raw=true)

K-ö-l-n
![](https://github.com/Masub27/Thesis-collection/blob/main/Ko%CC%88ln.jpg?raw=true)

S-t-u-t-t-g-a-r-t
![](https://github.com/Masub27/Thesis-collection/blob/main/stuttgart_schlossplatz.jpg?raw=true)



# Horen Sie die Zahlen und sprechen Sie nach. 

?[](https://github.com/Masub27/Thesis-collection/blob/main/KursDaF_A1_KB_Track_004.mp3?raw=true)
<div style="
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.2;
    font-size: 8em;
    color: grey;
    z-index: 1000;
">
    Masub
</div>

| Zahl | Deutsch    | Aussprache       |
|------|------------|------------------|
| 1    | eins       | [aɪns]           |
| 2    | zwei       | [tsvaɪ]          |
| 3    | drei       | [dʁaɪ]           |
| 4    | vier       | [fiːɐ̯]           |
| 5    | fünf       | [fʏnf]           |
| 6    | sechs      | [zɛks]           |
| 7    | sieben     | [ˈziːbn̩]         |
| 8    | acht       | [axt]            |
| 9    | neun       | [nɔɪ̯n]           |
| 10   | zehn       | [tseːn]          |

# Horen Sie und schreiben Sie die Namen
<div style="
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.2;
    font-size: 8em;
    color: grey;
    z-index: 1000;
">
    Masub
</div>

?[](https://github.com/Masub27/Thesis-collection/blob/main/KursDaF_A1_KB_Track_003.mp3?raw=true)

1)Nelson [[M]][[u]][[l]][[l]][[e]][[r]]

2)Christen [[s]][[e]][[i]][[d]][[e]][[l]]

 ## Horen und Schreiben Sie die Telefonnummern.

 ?[](https://github.com/Masub27/Thesis-collection/blob/main/KursDaF_A1_KB_Track_005.mp3?raw=true)

1)Arek [[5]][[6]][[0]][[3]][[9]][[4]][[1]] 

2)Linus [[2]][[7]][[8]][[0]][[1]][[4]][[8]]    

3)Ella [[3]][[0]][[7]][[4]][[9]][[2]][[8]]   
# Speeking practice
<div style="
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.2;
    font-size: 8em;
    color: grey;
    z-index: 1000;
">
    Masub
</div>
   --{{0}}--
!?[](https://github.com/Masub27/Intro/blob/main/speek%201.mp4?raw=true)


**1) In English, we say "Hello!" In German, we say: Hallo!**

**2) In the morning, we say "Good morning!" In German, that’s: Guten Morgen!**

**3) In the afternoon, we say "Good day!" or "Good afternoon!" In German, it's: Guten Tag!**

**4) In the evening, we say "Good evening!" The German phrase is: Guten Abend!**

**5) At night, before sleeping, we say "Good night!" In German, we say: Gute Nacht!**

**Now let’s learn how to say goodbye. When you leave, you can say:**

**6) In English: "Goodbye!" In German: Auf Wiedersehen!**

**7) If you're just saying a casual "Bye!", you can say: Tschüss!**
# Test
<div style="
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0.2;
    font-size: 8em;
    color: grey;
    z-index: 1000;
">
    Masub
</div>
<!-- data-solution-button="off" -->

What about "Good Morning" in German? 

[[!]]
@SpeechRecognition(de-DE,`Guten Morgen`)
---
How to pronounced "Good afternoon" in german?

[[!]]
@SpeechRecognition(de-DE,`Guten Tag`)
---

How to pronounced "Good evening" in german?

[[!]]
@SpeechRecognition(de-DE,`Guten Abend`)

---

How to pronounced "Good night" in german?

[[!]]
@SpeechRecognition(de-DE,`Gute Nacht`)
---

How to pronounced "Bye" in german?

[[!]]
@SpeechRecognition(de-DE,`Tschüss`)
---

How to pronounced "See you later" in german?

[[!]]
@SpeechRecognition(de-DE,`Bis später`)

---

How to pronounced "See you tomorrow" in german?

[[!]]
@SpeechRecognition(de-DE,`Bis morgen`)
---

How to pronounced "What is your name?" in german?

[[!]]
@SpeechRecognition(de-DE,`Wie heißt du?`)
---

How to pronounced "Where are you from?" in german?

[[!]]
@SpeechRecognition(de-DE,`Woher kommst du?`)
---

How to pronounced "How are you?" in german?

[[!]]
@SpeechRecognition(de-DE,`Wie geht es dir?`)
---

How to pronounced "Do you speak English?" in german?

[[!]]
@SpeechRecognition(de-DE,`Sprichst du Englisch?`)
---

How to pronounced "Where do you live?" in german?

[[!]]
@SpeechRecognition(de-DE,`Wo wohnst du?`)
---

How to pronounced "What is this?" in german?

[[!]]
@SpeechRecognition(de-DE,`Was ist das?`)
---

How to pronounced "Thank you" in german?

[[!]]
@SpeechRecognition(de-DE,`Danke`)
---

How to pronounced "you are welcome" in german?

[[!]]
@SpeechRecognition(de-DE,`Gern geschehen`)
---

How to pronounced "Excuse me" in german?

[[!]]
@SpeechRecognition(de-DE,`Entschuldigung`)
---

How to pronounced "sorry" in german?

[[!]]
@SpeechRecognition(de-DE,`Es tut mir leid`)
---

How to pronounced "Please" in german?

[[!]]
@SpeechRecognition(de-DE,`Bitte`)
---

How to pronounced "Twenty-one" in german?

[[!]]
@SpeechRecognition(de-DE,`einundzwanzig`)
---






















