<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>نظام حجز المواعيد الطبية</title>
    <style>
        body {
            font-family: 'Tahoma', sans-serif;
            background-color: #f5f5f5;
            text-align: center;
            direction: rtl;
        }
        h1 {
            color: #2b7a78;
        }
        .container {
            background: white;
            width: 60%;
            margin: auto;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 2px 10px rgba(0,0,0,0.1);
        }
        form {
            margin-bottom: 20px;
        }
        input, select, button {
            padding: 10px;
            margin: 5px;
            border-radius: 8px;
            border: 1px solid #ccc;
        }
        button {
            background-color: #2b7a78;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #3aafa9;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🩺 نظام حجز المواعيد الطبية</h1>

        <!-- تسجيل مستخدم -->
        <h2>تسجيل مستخدم جديد</h2>
        <form action="register.php" method="POST">
            <input type="text" name="name" placeholder="الاسم الكامل" required>
            <input type="email" name="email" placeholder="البريد الإلكتروني" required>
            <button type="submit">تسجيل</button>
        </form>

        <!-- عرض الأطباء -->
        <h2>الأطباء المتاحين</h2>
        <table border="1" width="100%" style="border-collapse: collapse;">
            <tr style="background-color:#def;">
                <th>الرقم</th>
                <th>الاسم</th>
                <th>المواعيد المتاحة</th>
            </tr>
            <tr>
                <td>1</td>
                <td>د. أحمد</td>
                <td>2025-11-10 10:00, 2025-11-10 11:00</td>
            </tr>
            <tr>
                <td>2</td>
                <td>د. سارة</td>
                <td>2025-11-11 14:00, 2025-11-11 15:00</td>
            </tr>
        </table>

        <!-- حجز موعد -->
        <h2>حجز موعد</h2>
        <form action="book.php" method="POST">
            <input type="number" name="user_id" placeholder="رقم المستخدم" required>
            <select name="doctor_id">
                <option value="1">د. أحمد</option>
                <option value="2">د. سارة</option>
            </select>
            <input type="datetime-local" name="slot" required>
            <button type="submit">احجز الآن</button>
        </form>
    </div>
</body>
</html>
