Втора лабараториска вежба по Софтверско инженерство
Магдалена Попеска, 223022
2. Control Flow Graph

![Screenshot (956)](https://github.com/magdalenapopeska/SI_2024_lab2_223022/assets/165606684/26871448-5704-4560-8cfa-a3db8cac91f3)

3. Цикломатска комплекснот
M=E-N+2P E-број на рабови N-број на јазли P-број на поврзани компоненти M=48-40+2=10 M=10

4. Тест случаи според Every Branch
1. allItems == null - ќе се фрли исклучок 
2. name == null и barcode == null - name ќе е unknown, а за barcode ќе се фрли исклучок
3. name == null barcode=123bc - name ќе е unknown, а за barcode ќе се фрли исклучок затоа што има карактер
4. name == null barcode=123 discount=0.5 price=200 payment=100 - name ќе е unknown, barcode e 123, сумата е 200*0.5=100 и ќе се намали за 30 при што ќе изнесува 100-30=70 и бидејќи payment е поголем ќе врати true
5. name == null barcode=123 discount=0 price=200 payment=50 - name ќе е unknown, barcode e 123, сумата=200 payment е помал од сумата ќе врати false
   
5. Тест случаи според Multiple Condition
1. if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0') -
    T T T: price=400, discount=0.5, barcode=123 ќе врати true;
    T T F: price=400, discount=0.5, barcode=123bc грешно е затоа што во баркод има карактер ќе врати false;
    T F T/F: price=400, discount=1, barcode нема ни да го гледа ќе врати false;
    F T/F T/F: price=200, без разлика кој и да се вредностите на discount и barcode ќе врати false;



   
