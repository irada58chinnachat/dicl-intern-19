### DICL Internship Program 2019

สวัสดีน้องๆที่ให้ความสนใจมาฝึกงานที่บริษัท ดิจิตอล อินไซด์เดอร์ จำกัด ในปี 2019 นี้ทุกๆคนนะครับ ก่อนที่จะเข้ามาฝึกงานกับเรา พี่มีบททดสอบเล็กน้อยเพื่อวัดทักษะพื้นฐานและทำความรู้จักกัน และพี่อยากให้น้องๆทุกคนลองทำด้วยตัวเอง ค้นคว้าเอง ไม่ถูกต้องไม่เป็นไรนะครับ พราะเรามาสามารถมาเรียนรู้กันภายหลังได้ หากใครสนใจส่งคำตอบกันมานะได้เลยนะครับ ปิดรับสมัครวันที่ 15 มีนาคม 2019 เวลา 23:59 น.

## 1. Coding ด้วยภาษาอะไรก็ได้
แบบทดสอบนี้จะดูทักษะความรู้ความเข้าใจเกี่ยวกับเรื่อง Collection เช่น Array, Dictionary เป็นต้น

ดาวน์โหลดข้อมูล [data.json](https://github.com/memogames/dicl-intern-18/blob/master/data.json) และเขียนโค้ดเพื่อหาคำตอบ
- 1.1 หาคะแนนเฉลี่ย **score** ของนักเรียน
- 1.2 แสดงชื่อและเกรดของนักเรียนที่ได้คะแนนมากว่า 70 ขึ้นไป
- 1.3 ค้นหาชื่อนักเรียนที่มีคะแนนมากที่สุดและต่ำที่สุด **score**

คำตอบ:
```
ScoreStudent.php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>

   
</head>
<body>
    
<a href="test.php">ค่าเฉลี่ย</a><br>
<a href="test1_2.php">คะแนนมากกว่า70</a><br>
<a href="max.php">นักเรียนที่มีคะแนนมากที่สุด</a><br>
<a href="min.php">นักเรียนที่มีคะแนนน้อยที่สุด</a><br>
    
</body>



</html>


avg.php
<?php

$str = file_get_contents('data.json');
$json = json_decode($str, true); 
//echo '<pre>' . print_r($json, true) . '</pre>';
$temperatureMin = $json[1]['name'];
///echo $temperatureMin ;


$result = sizeof($json); 
  
for ($i=0; $i < $result; $i++) { 
  $ar[$i]=$json[$i]['score'];
}
$avg = array_sum($ar)/ count($ar);
echo $avg
  
?>


test1_2.php

<?php

$str = file_get_contents('data.json');
$json = json_decode($str, true); 
//echo '<pre>' . print_r($json, true) . '</pre>';
$temperatureMin = $json[1]['name'];
///echo $temperatureMin ;

$result = sizeof($json); 
  
for ($i=0; $i < $result; $i++) { 
  $score = $json[$i]['score'];
  if ($score >70) {
      
      echo "ชื่อ : ".$json[$i]['name'];
      echo "<br>";
      echo "เกรด : ".$json[$i]['grade'];
      echo "<br>";
      echo "<br>";
  }
}

  
?>

min.php
<?php

$str = file_get_contents('data.json');
$json = json_decode($str, true); 
//echo '<pre>' . print_r($json, true) . '</pre>';
$temperatureMin = $json[1]['name'];
///echo $temperatureMin ;


$result = sizeof($json); 
  
for ($i=0; $i < $result; $i++) { 
  $ar[$i]=$json[$i]['score'];
}

$min= (min($ar));

for ($i=0; $i < $result; $i++) { 
    $score = $json[$i]['score'];
    if ($score ==$min ) {
        
        echo "ชื่อ : ".$json[$i]['name'];
        echo "<br>";
        echo "<br>";
    }
  }
?>


max.php
<?php

$str = file_get_contents('data.json');
$json = json_decode($str, true); 
//echo '<pre>' . print_r($json, true) . '</pre>';
$temperatureMin = $json[1]['name'];
///echo $temperatureMin ;


$result = sizeof($json); 
  
for ($i=0; $i < $result; $i++) { 
  $ar[$i]=$json[$i]['score'];
}

$max= (max($ar));

for ($i=0; $i < $result; $i++) { 
    $score = $json[$i]['score'];
    if ($score ==$max ) {
        
        echo "ชื่อ : ".$json[$i]['name'];
        echo "<br>";
        echo "<br>";
    }
  }
?>




```

## 2. Create Simple Application (Web App หรือ Mobile App)

แบบทดสอบนี้จะดูทักษะความรู้ความเข้าใจสำหรับการพัฒนาแอปพลิเคชั่น และการใช้ UI พื้นฐานของแต่ละ Platform

### Features
- GET ข้อมูล JSON จาก [movie.json](https://github.com/memogames/dicl-intern-18/blob/master/movie.json)
- แสดงรายชื่อและรูปภาพ
- ผู้ใช้สามารถกดเพื่อดูข้อมูลรายละเอียดได้ในหน้าถัดไป
- ผู้ใช้สามารถแชร์ข้อมูลชื่อหนังที่สนใจให้กับเพื่อนๆได้
- ออกแบบ UI ได้ตามความต้องการ
- สามารถใช้ Library เพิิ่มเติิมได้

### Technical
- ดาวน์โหลดข้อมูล JSON
- เครื่องมือที่ใช้ Android Studio, Xcode หรือ VSCode

## 3. Question

Question 1: Firebase คืออะไร มีฟังก์ชั่นที่น้องๆชื่นชอบนอะไรบ้างและเพราะอะไร (อย่างน้อย 3 ฟังก์ชั่น)

```
Answer 1: Firebase เป็นฐานข้อมูล เป็น Project ที่ถูกออกแบบมาให้เป็น API และ Cloud Storage สำหรับพัฒนา Realtime Application ฟังก์ชั่นที่คิดว่าชอบคือ 
  - Firebase Invites เพราะ น่าจะดึงดูดให้คนเข้ามาใช้ได้มากขึ้น
  - Firebase Crash Reporting คิดว่าน่าจะสะดวกในการใช้งาน
  - Firebase Test Lab for Android เพราะช่วนให้มั่นใจในการทำงานของผลงานที่สร้างขึ้น
```

Question 2: REST API คืออะไร

```
Answer 2: RESTful หรือ REST ย่อมาจาก Representational state transfer หรือ REST เป็น API อย่างหนึ่ง เป็นการสร้าง Webservice ชนิดหนึ่งที่ใช้สื่อสารกันบน Internet ใช้หลักการแบบ stateless  คือไม่มี session ซึ่งต่างจาก webservice แบบอื่นเช่น WSDL และ SOAP การทำงานของ RESTful Webservice จะอาศัย URI/URL ของ request เพื่อค้นหาและประมวลผลแล้วตอบกลับไปในรูป XML, HTML, JSON  โดย response ที่ตอบกลับจะเป็นการยืนยันผลของคำสั่งที่ส่งมา และสามารถพัฒนาด้วยภาษา programming ได้หลากหลาย คำสั่งก็จะมีตาม HTTP verbs ซึ่งก็คือ

    GET ทำกการดึงข้อมูลภายใน URI ที่กำหนด
    POST สำหรับสร้างข้อมูล
    PUT ใช้แก้ไขข้อมูล
    DELETE สำหรับลบข้อมูล
```

Question 3: หากต้องสร้างแอปพลิเคชั่น 1 ตัว เพื่อให้รองรับทั้งระบบ iOS และ Android วิิธีไหนที่น้องๆอยากเลือกใช้พัฒนาระหว่าง Native App กับ Cross Platform และเพราะอะไร 

```
Answer 3:Cross Platform เพราะเขียนครั้งเดียวใช้ได้หลาย platform
```

Question 4: ถ้าให้เลือกได้ 1 ค่าย น้องๆอยากเป็นสาวกค่ายไหนระหว่าง Apple , Google , Microsoft หรือขอไม่เลือกเลย

```
Answer 4: ไม่เลือกเลย ได้หมด ใช้ผลิตภัณฑ์ได้หมดทุกค่ายถ้ามีเงินซื้อมาใช้ หรือได้ฟรี
```

Question 5: สิ่งที่ชอบทำมากสุดเวลาว่างคืออะไร (2 อันดับแรก)

```
Answer 5: หาวิธีทำขนมให้อร่อยถูกมาตรฐานแล้วขายยังไงให้ได้กำไรเยอะๆกับอ่านแล้วก็แต่งนิยาย
```

Question 6: แอปพลิเคชั่นไหนที่ชอบที่สุดและไม่ชอบที่สุดตั้งแต่เคยใช้งานมา (ไม่นับเกมส์) เพราะอะไร

```
Answer 6: แอปที่ไม่ชอบที่สุดจำไม่ได้ว่าชื่อแอปอะไรแต่เป็นแอปที่ดูรายการโทรทัศน์ย้อนหลัง รายการใรแอปไม่อัปเดต ภาพเบลอ หลายวิดิโอก็ดูไม่ได้ หลายรายการก็หาไม่เจอ แอปที่ชอบที่สุดมีสองแอปคือแอปอ่านนิยายdek-dกับyoutube เพราะแอปหนึ่งใช้อ่านนิยายอีกแอปใช้ดูวิธีทำขนมหารายได้
```

Question 7: อะไรบ้างที่น้องๆคาดว่าจะได้รับในขณะที่ฝึกงานกับพวกเรา?

```
Answer 7:ความรู้ ประสบการณ์การทำงาน ได้ไอเดียใช้ทำโปรเจค และแนวทางในการทำงานในอนาคต
```

## Submitting

ให้ fork repo นี้แล้วตอบคำถาม จากนั้นส่ง repo มาที่ อีเมลล์ memo.games@gmail.com และ x10geeky@gmail.com
