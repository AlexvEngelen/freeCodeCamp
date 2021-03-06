---
title: File System
localeTitle: نظام الملفات
---
## نظام الملفات

تسمح لك وحدة نظام الملفات Node.js بالعمل مع نظام الملفات على جهاز الكمبيوتر الخاص بك.

يحتوي Node.js على مجموعة من الوحدات المضمنة التي يمكنك استخدامها بدون أي تثبيت إضافي. وبالمثل ، تحتوي **وحدة نظام الملفات** على مجموعة من الوظائف المطلوبة لأداء عمليات مختلفة على الملفات مثل القراءة والكتابة.

من أجل تضمين وحدة نمطية ، استخدم الدالة `require()` مع اسم الوحدة.

 `const fs = require('fs');
`

الاستخدام الشائع لوحدة نظام الملفات:

*   قراءة الملفات
*   إنشاء ملفات
*   تحديث الملفات
*   حذف الملفات
*   إعادة تسمية الملفات

## قراءة ملف

يتم استخدام الأسلوب `fs.readFile()` لقراءة الملف على جهاز الكمبيوتر الخاص بك. يستغرق ثلاث حجج - اسم الملف ، الترميز ووظيفة معاودة الاتصال.

رمز Node.js لقراءة الملف من جهاز الكمبيوتر وإرجاع المحتوى إلى وحدة التحكم.

 `const fs = require('fs');
 fs.readFile('input.txt', 'utf-8', (err, data) => {
  if(err){
  console.log(err);
  }
  else{
  console.log("Content present in input.txt file : " + data.toString());
  }
 });
`

يقرأ الكود أعلاه ملف _input.txt_ من جهاز الكمبيوتر ويعيد المحتوى إلى وحدة التحكم.

### خطوات التنفيذ:

*   يجب أن يكون لديك Node.js مثبتًا في جهاز الكمبيوتر الخاص بك.
*   قم بإنشاء ملف _app.js_ وقم بلصق الكود أعلاه.
*   قم بإنشاء ملف _input.txt_ واكتب بعض المحتويات فيه.
*   الآن افتح وحدة التحكم الخاصة بك في دليل العمل وتنفيذ `node app.js` الأوامر `node app.js`

_ملاحظة_ : يجب أن يكون ملف input.txt موجودًا في نفس الدليل حيث يوجد ملف شفرة Node.js الخاص بك ، وإلا فسيتم إلقاء خطأ.

## الكتابة في ملف

`fs.writeFile()` ثلاث وسائط - اسم الملف والمحتوى ووظيفة معاودة الاتصال.

رمز Node.js لكتابة المحتوى في ملف.

 `const fs = require('fs');
 fs.writeFile('output.txt', "New content added", (err, data) => {
    if(err){
        console.log(err);
    }
    else{
        console.log("The file is saved");
    }
 });
`

تعمل الشفرة الموضحة أعلاه على إنشاء ملف _output.txt_ ومحتوى إضافة محتوى _جديد تمت إضافته_ إليه.

### خطوات التنفيذ:

*   يجب أن يكون لديك Node.js مثبتًا في جهاز الكمبيوتر الخاص بك.
*   قم بإنشاء ملف _app.js_ وقم بلصق الكود أعلاه.
*   الآن افتح وحدة التحكم الخاصة بك في دليل العمل وتنفيذ `node app.js` الأوامر `node app.js`

_ملاحظة_ : إذا كان الملف غير موجود ، فإن الطريقة `fs.writeFile()` تنشئ ملفًا وتكتب المحتوى فيه. على العكس من ذلك ، إذا كان الملف موجودًا ، فسيقوم بالكتابة فوق المحتوى الموجود في الملف.

## مصادر

*   [Node.js API](https://nodejs.org/api/fs.html#fs_file_system)
*   [مدارس W3](https://www.w3schools.com/nodejs/nodejs_filesystem.asp)