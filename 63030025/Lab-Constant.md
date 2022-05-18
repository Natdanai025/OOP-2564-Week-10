# การทดลอง Constants #

## การทดลอง 10.3 Constants ##

1. ให้นักศึกษาสร้าง project ชนิด Console application แล้วเขียน code ต่อไปนี้

``` cs
using System;
class Circle
{
    public const double PI = 3.14;
    static public void CalculateArea(double radius)
    {
        Console.WriteLine($"Area of circle = {PI * radius * radius} square unit.");
    }
    
}
class Program
{
    static void Main()
    {
        Circle.CalculateArea(radius: 10.0);
    }
}
```

2. บันทึกผลจากการรันโปรแกรม
![image](https://user-images.githubusercontent.com/92078990/168983856-e7c4b33e-58cf-4e3e-a95b-44a322738f13.png)

4. ค่า PI จากตัวอย่างที่แล้ว เป็นค่าโดยประมาณที่ขาดความละเอียด จึงได้กดเครื่องคิดเลข ได้ค่า PI มาเป็นทศนิยม 10 หลัก จึงนำมาใส่ในโปรแกรมแทนที่ค่า PI เดิม ก่อนหาพื้นที่

```cs
using System;
class Circle
{
    public const double PI = 3.14;
    static public void CalculateArea(double radius)
    {
        // คำนวณจากเครื่องคิดเลข ได้ค่าที่ละเอียดกว่า จึงนำมาเปลี่ยนก่อนคำนวณพื้นที่
        PI = 3.14159265359;
        Console.WriteLine($"Area of circle = {PI * radius * radius} square unit.");
    }
    
}
class Program
{
    static void Main()
    {
        Circle.CalculateArea(radius: 10.0);
    }
}

```
4. บันทึกผลจากการรันโปรแกรม
![image](https://user-images.githubusercontent.com/92078990/168984172-dac6afe5-7019-436b-a7fc-66bb4386c5d8.png)

5. เปรียบเทียบและอธิบายสิ่งที่ได้จากการรันโปรแกรมในข้อ 1 และ ข้อ 3
ข้อ 1 สามารถรันโปรแกรมได้ปกติ เพราะประกาศตัวแปรแบบ ค่าคงที่ และไม่ได้มีการเปลี่ยนแปลงค่าหลังจากที่สร้าง และกำหนดค่าขึ้นมา
ข้อ 3 ไม่สามารถรันโปรแกรมได้ เพราะเนื่องจากเป็นการประกาศตัวแปรแบบค่าคงที่ การประกาศตัวแปรแบบค่าคงที่ จะไม่สามารถเปลี่ยนแปลงค่าได้ หลังจากถูกกำหนดค่าแล้ว
### คำถาม ###
1. โปรแกรมในข้อ 1 และ 3 สามารถทำงานได้ตามปกตือหรือไม่
โปรแกรมในข้อ 1 สามารภทำงานได้ปกติ
โปรแกรมในข้อ 3 ไม่สามารภทำงานได้
2. ข้อใดรันได้หรือไม่ได้
โปรแกรมในข้อ 1 สามารภรันโปรแกรมได้ปกติ
โปรแกรมในข้อ 3 ไม่สามารถรันโปรแกรมได้
3. ถ้าจะให้แก้ไขโปรแกรม ต้องแก้ที่จุดไหน อย่างไร
หากอยากได้ ค่าที่ละเอียดกว่าจะต้องนำค่าไป กำหนดในตัวแปรตั้งแต่แรก หรือ ไม่ใช้ตัวแปรแบบค่าคงที่ ก็จะสามารถเปลี่ยนแปลงค่าได้เช่นกัน
