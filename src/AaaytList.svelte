<script>
import Suraah from "./Suraah.svelte";
import App from "./App.svelte";

let suraahArr= 
[
  {
     suraahNum:1,suraahName:"Al-Fatihah",totalAayats:7,juz:"1"  },
  {
     suraahNum:2,suraahName:"Al-Baqarah",totalAayats:286,juz:"1-3"  },
  {
     suraahNum:3,suraahName:"Ali 'Imran",totalAayats:200,juz:"3-4"  },
  {
     suraahNum:4,suraahName:"An-Nisa",totalAayats:176,juz:"4-6"  },
  {
     suraahNum:5,suraahName:"Al-Ma'idah",totalAayats:120,juz:"6-7"  },
  {
     suraahNum:6,suraahName:"Al-An'am",totalAayats:165,juz:"7-8"  },
  {
     suraahNum:7,suraahName:"Al-A'raf",totalAayats:206,juz:"8-9"  },
  {
     suraahNum:8,suraahName:"Al-Anfal",totalAayats:75,juz:"9-10"  },
  {
     suraahNum:9,suraahName:"At-Tawbah",totalAayats:129,juz:"10-11"  },
  {
     suraahNum:10,suraahName:"Yunus",totalAayats:109,juz:"11"  },
  {
     suraahNum:11,suraahName:"Hud",totalAayats:123,juz:"11-12"  },
  {
     suraahNum:12,suraahName:"Yusuf",totalAayats:111,juz:"12-13"  },
  {
     suraahNum:13,suraahName:"Ar-Ra'd",totalAayats:43,juz:"13"  },
  {
     suraahNum:14,suraahName:"Ibrahim",totalAayats:52,juz:""  },
  {
     suraahNum:15,suraahName:"Al-Hijr",totalAayats:99,juz:"14"  },
  {
     suraahNum:16,suraahName:"An-Nahl",totalAayats:128,juz:""  },
  {
     suraahNum:17,suraahName:"Al-Isra",totalAayats:111,juz:"15"  },
  {
     suraahNum:18,suraahName:"Al-Kahf",totalAayats:110,juz:"15-16"  },
  {
     suraahNum:19,suraahName:"Maryam",totalAayats:98,juz:"16"  },
  {
     suraahNum:20,suraahName:"Ta-Ha",totalAayats:135,juz:""  },
  {
     suraahNum:21,suraahName:"Al-Anbiya",totalAayats:112,juz:"17"  },
  {
     suraahNum:22,suraahName:"Al-Hajj",totalAayats:78,juz:""  },
  {
     suraahNum:23,suraahName:"Al-Mu'minun",totalAayats:118,juz:"18"  },
  {
     suraahNum:24,suraahName:"An-Nur",totalAayats:64,juz:""  },
  {
     suraahNum:25,suraahName:"Al-Furqan",totalAayats:77,juz:"18-19"  },
  {
     suraahNum:26,suraahName:"Ash-Shu'ara",totalAayats:227,juz:"19"  },
  {
     suraahNum:27,suraahName:"An-Naml",totalAayats:93,juz:"19-20"  },
  {
     suraahNum:28,suraahName:"Al-Qasas",totalAayats:88,juz:"20"  },
  {
     suraahNum:29,suraahName:"Al-Ankabut",totalAayats:69,juz:"20-21"  },
  {
     suraahNum:30,suraahName:"Ar-Rum",totalAayats:60,juz:"21"  },
  {
     suraahNum:31,suraahName:"Luqmaan",totalAayats:34,juz:""  },
  {
     suraahNum:32,suraahName:"As-Sajdah",totalAayats:30,juz:""  },
  {
     suraahNum:33,suraahName:"Al-Ahzaab",totalAayats:73,juz:"21-22"  },
  {
     suraahNum:34,suraahName:"Saba (surah)",totalAayats:54,juz:"22"  },
  {
     suraahNum:35,suraahName:"Faatir",totalAayats:45,juz:""  },
  {
     suraahNum:36,suraahName:"Ya-Sin",totalAayats:83,juz:"22-23"  },
  {
     suraahNum:37,suraahName:"As-Saaffaat",totalAayats:182,juz:"23"  },
  {
     suraahNum:38,suraahName:"Saad",totalAayats:88,juz:""  },
  {
     suraahNum:39,suraahName:"Az-Zumar",totalAayats:75,juz:"23-24"  },
  {
     suraahNum:40,suraahName:"Ghafir",totalAayats:85,juz:"24"  },
  {
     suraahNum:41,suraahName:"Fussilat",totalAayats:54,juz:"24-25"  },
  {
     suraahNum:42,suraahName:"Ash-Shooraa",totalAayats:53,juz:"25"  },
  {
     suraahNum:43,suraahName:"Az-Zukhruf",totalAayats:89,juz:""  },
  {
     suraahNum:44,suraahName:"Ad-Dukhaan",totalAayats:59,juz:""  },
  {
     suraahNum:45,suraahName:"Al-Jaathiyah",totalAayats:37,juz:""  },
  {
     suraahNum:46,suraahName:"Al-Ahqaaf",totalAayats:"35 (4 1/2)",juz:"26"  },
  {
     suraahNum:47,suraahName:"Muhammad",totalAayats:38,juz:""  },
  {
     suraahNum:48,suraahName:"Al-Fath",totalAayats:"29 (4 1/2)",juz:""  },
  {
     suraahNum:49,suraahName:"Al-Hujuraat",totalAayats:"18 (2 1/2)",juz:""  },
  {
     suraahNum:50,suraahName:"Qaaf",totalAayats:45,juz:""  },
  {
     suraahNum:51,suraahName:"Adh-Dhaariyaat",totalAayats:"60 (2 1/2)",juz:"26-27"  },
  {
     suraahNum:52,suraahName:"At-Toor",totalAayats:"49 (2 1/2)",juz:"27"  },
  {
     suraahNum:53,suraahName:"An-Najm",totalAayats:"62 (2 1/2)",juz:""  },
  {
     suraahNum:54,suraahName:"Al-Qamar",totalAayats:"55 (2 1/2)",juz:""  },
  {
     suraahNum:55,suraahName:"Ar-Rahman",totalAayats:78,juz:""  },
  {
     suraahNum:56,suraahName:"Al-Waqi'a",totalAayats:"96 (3 1/2)",juz:""  },
  {
     suraahNum:57,suraahName:"Al-Hadeed",totalAayats:29,juz:""  },
  {
     suraahNum:58,suraahName:"Al-Mujadila",totalAayats:"22 (3 1/2)",juz:"28"  },
  {
     suraahNum:59,suraahName:"Al-Hashr",totalAayats:"24 (3 1/2)",juz:""  },
  {
     suraahNum:60,suraahName:"Al-Mumtahanah",totalAayats:"13 (2 1/2)",juz:""  },
  {
     suraahNum:61,suraahName:"As-Saff",totalAayats:"14 (1 1/2",juz:""  },
  {
     suraahNum:62,suraahName:"Al-Jumu'ah",totalAayats:"11 (1 1/2",juz:""  },
  {
     suraahNum:63,suraahName:"Al-Munafiqoon",totalAayats:"11 (1 1/2)",juz:""  },
  {
     suraahNum:64,suraahName:"At-Taghabun",totalAayats:18,juz:""  },
  {
     suraahNum:65,suraahName:"At-Talaq",totalAayats:12,juz:""  },
  {
     suraahNum:66,suraahName:"At-Tahreem",totalAayats:12,juz:""  },
  {
     suraahNum:67,suraahName:"Al-Mulk",totalAayats:"30 (1 1/2)",juz:"29"  },
  {
     suraahNum:68,suraahName:"Al-Qalam",totalAayats:52,juz:""  },
  {
     suraahNum:69,suraahName:"Al-Haaqqa",totalAayats:52,juz:""  },
  {
     suraahNum:70,suraahName:"Al-Ma'aarij",totalAayats:"44 (1 1/2)",juz:""  },
  {
     suraahNum:71,suraahName:"Nuh",totalAayats:"28 (1 1/2)",juz:""  },
  {
     suraahNum:72,suraahName:"Al-Jinn",totalAayats:28,juz:""  },
  {
     suraahNum:73,suraahName:"Al-Muzzammil",totalAayats:"20 (1 1/2)",juz:""  },
  {
     suraahNum:74,suraahName:"Al-Muddaththir",totalAayats:56,juz:""  },
  {
     suraahNum:75,suraahName:"Al-Qiyamah",totalAayats:40,juz:""  },
  {
     suraahNum:76,suraahName:"Al-Insaan",totalAayats:31,juz:""  },
  {
     suraahNum:77,suraahName:"Al-Mursalaat",totalAayats:"50 (1 1/2)",juz:""  },
  {
     suraahNum:78,suraahName:"An-Naba'",totalAayats:"40 (1 1/2)",juz:"30"  },
  {
     suraahNum:79,suraahName:"An-Naazi'aat",totalAayats:"46 (1 1/2)",juz:""  },
  {
     suraahNum:80,suraahName:"Abasa",totalAayats:42,juz:""  },
  {
     suraahNum:81,suraahName:"At-Takweer",totalAayats:29,juz:""  },
  {
     suraahNum:82,suraahName:"Al-Infitar",totalAayats:19,juz:""  },
  {
     suraahNum:83,suraahName:"Al-Mutaffifeen",totalAayats:36,juz:""  },
  {
     suraahNum:84,suraahName:"Al-Inshiqaaq",totalAayats:25,juz:""  },
  {
     suraahNum:85,suraahName:"Al-Burooj",totalAayats:22,juz:""  },
  {
     suraahNum:86,suraahName:"At-Taariq",totalAayats:17,juz:""  },
  {
     suraahNum:87,suraahName:"Al-A'la",totalAayats:19,juz:""  },
  {
     suraahNum:88,suraahName:"Al-Ghaashiyah",totalAayats:26,juz:""  },
  {
     suraahNum:89,suraahName:"Al-Fajr",totalAayats:30,juz:""  },
  {
     suraahNum:90,suraahName:"Al-Balad",totalAayats:20,juz:""  },
  {
     suraahNum:91,suraahName:"Ash-Shams",totalAayats:15,juz:""  },
  {
     suraahNum:92,suraahName:"Al-Layl",totalAayats:21,juz:""  },
  {
     suraahNum:93,suraahName:"Ad-Dhuha",totalAayats:11,juz:""  },
  {
     suraahNum:94,suraahName:"Ash-Sharh (Al-Inshirah)",totalAayats:8,juz:""  },
  {
     suraahNum:95,suraahName:"At-Tin",totalAayats:8,juz:""  },
  {
     suraahNum:96,suraahName:"Al-Alaq",totalAayats:19,juz:""  },
  {
     suraahNum:97,suraahName:"Al-Qadr",totalAayats:5,juz:""  },
  {
     suraahNum:98,suraahName:"Al-Bayyinahh",totalAayats:8,juz:""  },
  {
     suraahNum:99,suraahName:"Az-Zalzalah",totalAayats:8,juz:""  },
  {
     suraahNum:100,suraahName:"Al-'Adiyat",totalAayats:11,juz:""  },
  {
     suraahNum:101,suraahName:"Al-Qaari'ah",totalAayats:11,juz:""  },
  {
     suraahNum:102,suraahName:"At-Takathur",totalAayats:8,juz:""  },
  {
     suraahNum:103,suraahName:"Al-'Asr",totalAayats:3,juz:""  },
  {
     suraahNum:104,suraahName:"Al-Humazah",totalAayats:9,juz:""  },
  {
     suraahNum:105,suraahName:"Al-Fil",totalAayats:5,juz:""  },
  {
     suraahNum:106,suraahName:"Quraysh",totalAayats:4,juz:""  },
  {
     suraahNum:107,suraahName:"Al-Maa'oon",totalAayats:7,juz:""  },
  {
     suraahNum:108,suraahName:"Al-Kawthar",totalAayats:3,juz:""  },
  {
     suraahNum:109,suraahName:"Al-Kaafiroon",totalAayats:6,juz:""  },
  {
     suraahNum:110,suraahName:"An-Nasr",totalAayats:3,juz:""  },
  {
     suraahNum:111,suraahName:"Al-Masad",totalAayats:5,juz:""  },
  {
     suraahNum:112,suraahName:"Al-Ikhlaas",totalAayats:4,juz:""  },
  {
     suraahNum:113,suraahName:"Al-Falaq",totalAayats:5,juz:""  },
  {
     suraahNum:114,suraahName:"An-Naas",totalAayats:6,juz:""  }
];

function sortSuraahByAaaytCount() {
    console.log("inside sort ");
    suraahArr = suraahArr.sort((a, b) => {
        return a.totalAayats- b.totalAayats;
    });
}
</script>

<button on:click={sortSuraahByAaaytCount}> Sort By total Aayats in Suraah</button>
<div class="aayatList">
    {#each suraahArr as suraah}
        <Suraah {...suraah}></Suraah>
    {/each}
</div>