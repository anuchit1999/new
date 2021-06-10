# PrompThink PEA (Demo Dashboard)

Dashboard demo โปรเจคท์การไฟฟ้า by Son, Frame, & Nu


## 1. ติดตั้งและรันโปรเจคท์

##### 1.1 Clone โปรเจคท์

```bash
git clone https://github.com/SonNavigator/vue-dashboard-demo.git
```

##### 1.2 ไปที่ working directory  (vue-black-dashboard-master)
```bash
cd vue-black-dashboard-master
```

##### 1.3 รันโปรเจคท์ผ่าน npm 

```bash
npm run serve
```

##### 1.4 ถ้ารันสำเร็จจะขึ้น URLs ด้านล่าง
```bash
  App running at:
  - Local:   http://localhost:8080/   
  - Network: http://192.168.1.19:8080/
```

Note: ถ้าขึ้น error ตามด้านล่าง
```bash
'vue-cli-service' is not recognized as an internal or external command,
operable program or batch file.

```
ให้ทำการรัน
```bash
npm i
```
จากนั้น npm run serve อีกครั้ง




## 2. แยก branch เพื่อทำฟีเจอร์นั้น ๆ 

##### 2.1 ทำการแยก branch
ต้องมีการแยก branch ออกจาก main ซึ่งเป็น remote branch (branch ที่เป็นโค้ดสมบูรณ์และใช้ deploy)
ซึ่งเมื่อมีการพัฒนาหรือแก้ไขฟีเจอร์ไหนก็สามารถสร้าง branch ใหม่ตามชื่อฟีเจอร์นั้นได้เลย
ตัวอย่างเช่น กำลังสร้างหน้าไฟล์ vue เพื่อดึง API จาก Django REST ก็สร้าง branch ชื่อ get_djangoapi
```bash
git checkout -b get_djangoapi
```

หรือใช้ตัวย่อ "co" แทนคำว่า checkout ก็ได้เช่นกัน
```bash
git co -b get_djangoapi
```

เช็คสถานะว่าอยู่ใน branch นี้หรือยังด้วยคำสั่ง
```bash
git branch
```
ถ้าอยู่ใน branch ที่สร้างขึ้นเมื่อสักครู่คือ get_djangoapi ก็จะขึ้นตามด้านล่าง
ซึ่ง branch ที่เรากำลังทำงานอยู่จะแสดง * นำหน้า
```bash
main
* get_djangoapi
```


## 3. คำสั่ง GitHub ที่ต้องใช้และควรรู้

##### 3.1 ทำการเริ่มต้น Git
```bash
git init
```

ทำการเช็ค status 
```bash
git status
```

และจะพบว่าตอนนี้ยังไม่ได้มีการเปลี่ยนแปลงอะไร
```bash
no changes added to commit (use "git add" and/or "git commit -a")
```
จากนั้นให้ทำการเปลี่ยนแปลงอะไรก็ได้สักไฟล์ เช่นในไฟล์ README.md ลองทำการเปลี่ยนแปลงอะไรสักอย่าง

##### 3.2 เมื่อมีการแก้ไขไฟล์และต้องการอัปเดตสิ่งที่แก้ไปด้วยคำสั่ง 
```bash
git add --all
```
หรือ "." (dot) ก็ได้เช่นกัน
```bash
git add .
```
##### 3.3 ทำการบอกว่า เราได้แก้หรืออัปเดตอะไรไปด้วย commit message เช่น
```bash
git commit -m "เพิ่ม title ของ dashboard"
```

##### 4.4 ส่งโค้ดขึ้น repo ของ get_djangoapi branch (เป็นคำสั่งในการ push ครั้งแรกของ branch) ก่อนทำการ pull request ในลำดับถัดไป
```bash
git push --set-upstream origin get_djangoapi
```

Note: ครั้งถัดไปสามารถใช้คำสั่งสั้น ๆ คือ push ได้เลยไม่ต้อง set upstream
```bash
git push
```


## 4. ทำการ pull request 
##### 4.1 ทำการ pull request
เมื่อทำการแก้ไขฟีเจอร์นั้นเสร็จสิ้นแล้วหรือเขียนโค้ดและทดสอบเสร็จสิ้น และมั่นใจว่าโค้ดทำงานถูกต้อง
ก็ให้ทำการ pull-request เพื่อขอรวมโค้ดเข้าไปที่ main (remote branch)
รอผู้ที่สร้าง repo (author --> SonNavigator) ทำการรีวิวเพื่อ merge (ผสานซอร์สโค้ดเข้าด้วยกัน)


## 5. ทำการ merge pull request 

#### 5.1 เลือก "Pull requests" 
![Pull request](https://github.com/SonNavigator/vue-dashboard-demo/blob/main/src/assets/demo/pr1.png?raw=true)

#### 5.2 ทำการ New pull request
![Pull request](https://github.com/SonNavigator/vue-dashboard-demo/blob/main/src/assets/demo/pr2.png?raw=true)

#### 5.3ทำการเปรียบเทียบ (Compare) branch ที่สร้างใหม่และ main (remote branch) โดยคอมเมนต์เข้าไป จากนั้นคลิก "Create pull request"
![Pull request](https://github.com/SonNavigator/vue-dashboard-demo/blob/main/src/assets/demo/pr4.png?raw=true)

#### 5.4 ทำการ Create pull request และเปรียบเทียบ (Compare) branch ที่สร้างใหม่และ main (remote branch)
![Pull request](https://github.com/SonNavigator/vue-dashboard-demo/blob/main/src/assets/demo/pr5.png?raw=true)

#### 5.5 ถ้าไม่มี conflict หรือปัญหา ก็สามารถกด "Merge pull request" ได้เลย
![Pull request](https://github.com/SonNavigator/vue-dashboard-demo/blob/main/src/assets/demo/pr6.png?raw=true)

#### สำเร็จ สามารถลบ branch ทิ้งได้เลย
![Pull request](https://github.com/SonNavigator/vue-dashboard-demo/blob/main/src/assets/demo/pr7.png?raw=true)

## ลิ้งค์บทความหรือคลิปวิดีโอเรียนรู้ที่แนะนำเพิ่มเติม
เรียนรู้พื้นฐานคำสั่ง Vue จาก Vue.js doc
[Vue.js - Documentaion](https://vuejs.org/v2/guide/)

พื้นฐานโครงสร้างของ Chart.js จาก Chart.js doc
[Chart.js - Documentaion](https://www.chartjs.org/docs/latest/)

ปล.ถ้ามีลิ้งค์ศึกษาที่เกี่ยวข้องเพิ่มเติม สามารถเพิ่มและ pull-request มาได้ทันที


## Documentation
[Vue Black Dashboard - doc](https://demos.creative-tim.com/vue-black-dashboard/documentation/)


