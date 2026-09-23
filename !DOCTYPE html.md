<div dir="rtl"># </div>  
<!DOCTYPE html>  
<html lang="ar" dir="rtl">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>**منظومة** **الدفع** **الإلكتروني** - **جامعة** **كفر** **الشيخ**</title>  
    <style>  
        * {  
            box-sizing: border-box;  
            margin: 0;  
            padding: 0;  
            font-family: Arial, sans-serif;  
        }  
        body {  
            background-color: #f4f5f7;  
            color: #333;  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            min-height: 100vh;  
        }  
        .container {  
            width: 100%;  
            max-width: 480px;  
            background: #ffffff;  
            min-height: 100vh;  
            box-shadow: 0 0 15px rgba(0,0,0,0.1);  
            display: flex;  
            flex-direction: column;  
        }  
        .top-header {  
            background: linear-gradient(135deg, #1b365d, #28518f);  
            color: white;  
            padding: 10px 15px;  
            display: flex;  
            justify-content: space-between;  
            align-items: center;  
            font-size: 13px;  
        }  
        .top-header .lang-switch {  
            background: rgba(255,255,255,0.2);  
            padding: 3px 8px;  
            border-radius: 3px;  
            cursor: pointer;  
        }  
        .content {  
            padding: 20px;  
            flex: 1;  
            display: flex;  
            flex-direction: column;  
            align-items: center;  
        }  
        .title {  
            font-size: 16px;  
            font-weight: bold;  
            margin: 15px 0;  
            text-align: center;  
            color: #222;  
        }  
        .stepper {  
            display: flex;  
            justify-content: space-between;  
            width: 80%;  
            margin: 10px 0 20px 0;  
            position: relative;  
        }  
        .step-indicator {  
            width: 28px;  
            height: 28px;  
            border-radius: 50%;  
            background-color: #e0e0e0;  
            color: #777;  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            font-size: 12px;  
            font-weight: bold;  
            z-index: 2;  
            border: 2px solid #fff;  
        }  
        .step-indicator.active {  
            background-color: #007bff;  
            color: white;  
        }  
        .step-indicator.completed {  
            background-color: #28a745;  
            color: white;  
        }  
        .stepper::before {  
            content: '';  
            position: absolute;  
            top: 50%;  
            left: 10%;  
            right: 10%;  
            height: 2px;  
            background-color: #e0e0e0;  
            transform: translateY(-50%);  
            z-index: 1;  
        }  
        .step-container {  
            width: 100%;  
            display: none;  
            flex-direction: column;  
            align-items: center;  
        }  
        .step-container.active {  
            display: flex;  
        }  
        .form-group {  
            width: 100%;  
            margin-bottom: 15px;  
        }  
        .form-group label {  
            display: block;  
            margin-bottom: 5px;  
            font-size: 14px;  
            color: #555;  
            text-align: right;  
        }  
        .form-control {  
            width: 100%;  
            padding: 10px;  
            border: 1px solid #ccc;  
            border-radius: 4px;  
            font-size: 14px;  
            text-align: right;  
        }  
        .error-msg {  
            color: #dc3545;  
            font-size: 12px;  
            margin-top: 4px;  
            text-align: right;  
            display: none;  
        }  
        .select-row {  
            display: flex;  
            gap: 10px;  
        }  
        .btn-container {  
            display: flex;  
            gap: 10px;  
            width: 100%;  
            margin-top: 20px;  
        }  
        .btn {  
            flex: 1;  
            padding: 10px;  
            border: none;  
            border-radius: 4px;  
            font-size: 15px;  
            cursor: pointer;  
            font-weight: bold;  
        }  
        .btn-primary {  
            background-color: #007bff;  
            color: white;  
        }  
        .btn-primary:disabled {  
            background-color: #cccccc;  
            cursor: not-allowed;  
        }  
        .btn-secondary {  
            background-color: #6c757d;  
            color: white;  
        }  
        .btn-danger {  
            background-color: #dc3545;  
            color: white;  
        }  
        .service-card {  
            border: 1px solid #dcdcdc;  
            border-radius: 12px;  
            padding: 25px 15px;  
            text-align: center;  
            width: 100%;  
            cursor: pointer;  
            background: #ffffff;  
            margin-top: 10px;  
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);  
            transition: all 0.2s;  
        }  
        .service-card:hover {  
            border-color: #007bff;  
            box-shadow: 0 4px 10px rgba(0,123,255,0.1);  
        }  
        .service-icon {  
            font-size: 32px;  
            margin-bottom: 10px;  
        }  
        .info-box {  
            background: #fff;  
            border: 1px solid #ccc;  
            border-radius: 6px;  
            padding: 15px;  
            width: 100%;  
            margin-bottom: 15px;  
            font-size: 14px;  
            line-height: 2;  
            text-align: right;  
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);  
        }  
        .info-row {  
            margin-bottom: 4px;  
        }  
        .info-label {  
            font-weight: normal;  
            color: #333;  
        }  
        .info-value {  
            font-weight: bold;  
            color: #111;  
        }  
        .warning-text {  
            color: #b8860b;  
            font-size: 12px;  
            text-align: center;  
            margin-bottom: 15px;  
            line-height: 1.5;  
            font-weight: bold;  
        }  
        .checkbox-group {  
            display: flex;  
            align-items: center;  
            gap: 8px;  
            width: 100%;  
            margin-bottom: 15px;  
            font-size: 13px;  
            text-align: right;  
        }  
        .section-title {  
            font-size: 15px;  
            font-weight: bold;  
            color: #1b365d;  
            margin: 15px 0 10px 0;  
            width: 100%;  
            text-align: right;  
        }  
        .summary-table {  
            width: 100%;  
            background: #fff;  
            border: 1px solid #ddd;  
            border-radius: 6px;  
            padding: 15px;  
            margin-top: 5px;  
        }  
        .summary-row {  
            display: flex;  
            justify-content: space-between;  
            padding: 8px 0;  
            border-bottom: 1px solid #eee;  
            font-size: 14px;  
        }  
        .summary-row:last-child {  
            border-bottom: none;  
            font-weight: bold;  
            color: #1b365d;  
        }  
    </style>  
</head>  
<body>  
  
<div class="container">  
    <!-- **البانر** **العلوي** **الثابت** -->  
    <div class="top-header" id="mainHeader">  
        <div>**منظومة** **الدفع** **الإلكتروني** - **جامعة** **كفر** **الشيخ**</div>  
        <div class="lang-switch">🌐 **العربية**</div>  
    </div>  
  
    <div class="content">  
        <div class="title" id="pageMainTitle">**دفع** **رسوم** **مقابل** **الخدمات** **المقدمة** **من** **الجامعة**</div>  
  
        <!-- **شريط** **تتبع** **المراحل** -->  
        <div class="stepper" id="stepperBar">  
            <div class="step-indicator active" id="ind1">1</div>  
            <div class="step-indicator" id="ind2">2</div>  
            <div class="step-indicator" id="ind3">3</div>  
            <div class="step-indicator" id="ind4">4</div>  
        </div>  
  
        <!-- **الخطوة** **الأولى**: **اختيار** **الخدمة** -->  
        <div id="step1" class="step-container active">  
            <div style="font-size: 13px; color: #666; margin-bottom: 10px; text-align: center;">**حدد** **الخدمة** **المراد** **دفع** **الرسوم** **الخاصة** **بها**</div>  
            <div class="service-card" onclick="goToStep(2)">  
                <div class="service-icon">🎓⚙️</div>  
                <div style="font-weight: bold; color: #1b365d; font-size: 14px;">**دفع** **الرسوم** **الدراسية** **لطلاب** **مرحلتي** **الليسانس** **والبكالوريوس**</div>  
            </div>  
        </div>  
  
        <!-- **الخطوة** **الثانية**: **الرقم** **القومي** -->  
        <div id="step2" class="step-container">  
            <div style="font-weight: bold; margin-bottom: 5px; font-size: 15px;">**هوية** **الطالب**</div>  
            <div style="font-size: 12px; color: #666; margin-bottom: 15px; text-align: center;">**برجاء** **إدخال** **الرقم** **القومي** **الخاص** **بك** **ثم** **اضغط** **متابعة**</div>  
            <div class="form-group">  
                <label>**الرقم** **القومي** *</label>  
                <input type="text" id="nationalId" class="form-control" placeholder="14 **رقم**" maxlength="14" oninput="validateNationalId()">  
                <div id="nationalIdError" class="error-msg">**يجب** **إدخال** **الرقم** **القومي** **صحيحاً** **ومكوناً** **من** 14 **رقماً**.</div>  
            </div>  
            <div class="btn-container">  
                <button class="btn btn-secondary" onclick="goToStep(1)">**رجوع**</button>  
                <button id="step2Btn" class="btn btn-primary" disabled onclick="validateAndNextStep2()">**متابعة**</button>  
            </div>  
        </div>  
  
        <!-- **الخطوة** **الثالثة**: **تأكيد** **الهوية** -->  
        <div id="step3" class="step-container">  
            <div style="font-weight: bold; margin-bottom: 5px; font-size: 15px; text-align: center;">**تأكيد** **الهوية**</div>  
            <div style="font-size: 12px; color: #444; margin-bottom: 8px; text-align: center;">**برجاء** **مراجعة** **وتأكيد** **صحة** **البيانات** **التالية** **الخاصة** **بك** **ثم** **الضغط** **متابعة**</div>  
            <div class="warning-text">**في** **حال** **وجود** **أي** **خطأ** **بالبيانات** **أو** **عدم** **مطابقتها،** **برجاء** **الضغط** **رجوع** **وإعادة** **كتابة** **الرقم** **القومي** **بصورة** **صحيحة**. **أو** **تواصل** **مع** **شئون** **الطلاب** **بكليتك**.</div>  
              
            <div class="info-box">  
                <div class="info-row"><span class="info-label">**كود** **الطالب**:</span> <span class="info-value">1611120230100213</span></div>  
                <div class="info-row"><span class="info-label">**اسم** **الطالب**:</span> <span class="info-value" style="font-size: 15px;">**يوسف** **شريف** **سعد** **الشريف**</span></div>  
                <div class="info-row"><span class="info-label">**الكلية** **التابع** **لها** **الطالب**:</span> <span class="info-value">**الصيدلة**</span></div>  
                <div class="info-row"><span class="info-label">**الفرقة**/**المستوى**:</span> <span class="info-value">**المستوى** **الثاني** (**عام**)</span></div>  
                <div class="info-row"><span class="info-label">**طبيعة** **الدراسة**:</span> <span class="info-value">**الانتظام**</span></div>  
                <div class="info-row"><span class="info-label">**العام** **الجامعي**:</span> <span class="info-value">2025-2024</span> <span style="color:red; font-size:12px; font-weight:bold;">(**عام** **جامعي** **سابق** **مستحق**)</span></div>  
            </div>  
  
            <div class="checkbox-group">  
                <input type="checkbox" id="confirmCheck" onchange="toggleConfirmBtn()">  
                <label for="confirmCheck" style="margin-bottom:0; cursor:pointer; font-weight: bold;">**أقر** **أن** **جميع** **بياناتي** **صحيحة** **وأرغب** **في** **الدفع** **الآن**.</label>  
            </div>  
  
            <div class="btn-container">  
                <button class="btn btn-secondary" onclick="goToStep(2)">**رجوع**</button>  
                <button id="step3Btn" class="btn btn-primary" disabled onclick="goToStep(4)">**متابعة**</button>  
            </div>  
        </div>  
  
        <!-- **الخطوة** **الرابعة**: **البريد** **ورقم** **الهاتف** -->  
        <div id="step4" class="step-container">  
            <div style="font-weight: bold; margin-bottom: 5px; font-size: 15px;">**الدفع**</div>  
            <div style="font-size: 12px; color: #666; margin-bottom: 15px; text-align: center;">**برجاء** **إدخال** **البيانات** **الإضافية** **ثم** **الضغط** **دفع**</div>  
              
            <div class="form-group">  
                <label>**البريد** **الإلكتروني** *</label>  
                <input type="email" id="emailInput" class="form-control" placeholder="example@domain.com" oninput="validateContactForm()">  
                <div id="emailError" class="error-msg">**يجب** **إدخال** **بريد** **إلكتروني** **صحيح** **وصالح** (**منتهي** **بـ** .com).</div>  
            </div>  
              
            <div class="form-group">  
                <label>**رقم** **الهاتف** **المحمول** *</label>  
                <input type="text" id="phoneInput" class="form-control" placeholder="01000000000" maxlength="11" oninput="validateContactForm()">  
                <div id="phoneError" class="error-msg">**يجب** **إدخال** **رقم** **هاتف** **محمول** **صحيح** **ومكون** **من** 11 **رقماً**.</div>  
            </div>  
  
            <div style="text-align: center; margin: 15px 0; font-weight: bold; color: #333;">  
                **المبلغ** **المستحق**: <span style="color: #007bff; font-size: 16px;">1,954.00 **ج**.**م**.</span>  
            </div>  
  
            <div class="btn-container">  
                <button class="btn btn-secondary" onclick="goToStep(3)">**رجوع**</button>  
                <button id="payBtn" class="btn btn-primary" disabled onclick="goToStep(5)">**دفع**</button>  
            </div>  
        </div>  
  
        <!-- **الخطوة** **الخامسة**: **صفحة** **الدفع** e-finance -->  
        <div id="step5" class="step-container">  
            <div class="section-title">**بيانات** **البطاقه**</div>  
              
            <div class="form-group">  
                <input type="text" class="form-control" placeholder="**رقم** **البطاقة**">  
            </div>  
  
            <div class="form-group">  
                <div class="select-row">  
                    <select class="form-control">  
                        <option>**شهر**</option>  
                        <option>01</option><option>02</option><option>03</option><option>04</option>  
                        <option>05</option><option>06</option><option>07</option><option>08</option>  
                        <option>09</option><option>10</option><option>11</option><option>12</option>  
                    </select>  
                    <select class="form-control">  
                        <option>**سنة**</option>  
                        <option>2026</option><option>2027</option><option>2028</option><option>2029</option><option>2030</option>  
                    </select>  
                </div>  
            </div>  
  
            <div class="form-group">  
                <input type="password" maxlength="4" class="form-control" placeholder="**رمز** **الأمان**">  
            </div>  
  
            <div class="checkbox-group" style="margin-bottom: 10px;">  
                <input type="checkbox" id="saveCard">  
                <label for="saveCard" style="margin-bottom:0; cursor:pointer;">**حفظ** **بيانات** **البطاقة**</label>  
            </div>  
  
            <div class="btn-container" style="margin-top: 5px; margin-bottom: 15px;">  
                <button class="btn btn-primary" style="background-color: #1b365d;" onclick="alert('**تمت** **محاكاة** **عملية** **الدفع** **بنجاح**!')">**ادفع**</button>  
                <button class="btn btn-danger" onclick="goToStep(4)">**العوده** **للسابق**</button>  
            </div>  
  
            <div class="section-title">**بيانات** **المدفوعة**</div>  
              
            <div class="summary-table">  
                <div class="summary-row"><span>**مقدم** **الخدمة**</span><span>**جامعة** **كفر** **الشيخ**</span></div>  
                <div class="summary-row"><span>**الخدمة**</span><span>**خدمات** **جامعة** **كفر** **الشيخ**</span></div>  
                <div class="summary-row"><span>**نوع** **المدفوعة**</span><span>**خدمات** **جامعة** **كفر** **الشيخ**</span></div>  
                <div class="summary-row"><span>**رقم** **المدفوعة**</span><span style="color:#007bff;">26092300006610</span></div>  
                <div class="summary-row"><span>**المبلغ**</span><span>1,954.00 **جنيه**</span></div>  
                <div class="summary-row"><span>**مقابل** **أداء** **الخدمة**</span><span>13.26 **جنيه**</span></div>  
                <div class="summary-row"><span>**إجمالي** **المبلغ**</span><span>1,967.26 **جنيه**</span></div>  
            </div>  
        </div>  
  
    </div>  
</div>  
  
<script>  
    function goToStep(stepNumber) {  
        document.querySelectorAll('.step-container').forEach(el => el.classList.remove('active'));  
        document.getElementById('step' + stepNumber).classList.add('active');  
          
        for (let i = 1; i <= 4; i++) {  
            const ind = document.getElementById('ind' + i);  
            if (ind) {  
                ind.className = 'step-indicator';  
                if (i < stepNumber) ind.classList.add('completed');  
                else if (i === stepNumber) ind.classList.add('active');  
            }  
        }  
  
        const header = document.getElementById('mainHeader');  
        const stepper = document.getElementById('stepperBar');  
        if (stepNumber === 5) {  
            header.innerHTML = '<div style="font-size:12px;">payment.efinance.com.eg</div><div>💳</div>';  
            document.getElementById('pageMainTitle').style.display = 'none';  
            if (stepper) stepper.style.display = 'none';  
        } else {  
            header.innerHTML = '<div>**منظومة** **الدفع** **الإلكتروني** - **جامعة** **كفر** **الشيخ**</div><div class="lang-switch">🌐 **العربية**</div>';  
            document.getElementById('pageMainTitle').style.display = 'block';  
            if (stepper) stepper.style.display = 'flex';  
        }  
        window.scrollTo(0, 0);  
    }  
  
    function validateNationalId() {  
        const val = document.getElementById('nationalId').value.trim();  
        const btn = document.getElementById('step2Btn');  
        const err = document.getElementById('nationalIdError');  
  
        const isNumeric = /^\d+$/.test(val);  
        if (val.length === 14 && isNumeric) {  
            btn.disabled = false;  
            err.style.display = 'none';  
        } else {  
            btn.disabled = true;  
            if (val.length > 0 && (val.length !== 14 || !isNumeric)) {  
                err.style.display = 'block';  
            } else {  
                err.style.display = 'none';  
            }  
        }  
    }  
  
    function validateAndNextStep2() {  
        const val = document.getElementById('nationalId').value.trim();  
        if (val.length === 14) {  
            goToStep(3);  
        }  
    }  
  
    function toggleConfirmBtn() {  
        const checked = document.getElementById('confirmCheck').checked;  
        document.getElementById('step3Btn').disabled = !checked;  
    }  
  
    function validateContactForm() {  
        const email = document.getElementById('emailInput').value.trim();  
        const phone = document.getElementById('phoneInput').value.trim();  
        const payBtn = document.getElementById('payBtn');  
          
        const emailErr = document.getElementById('emailError');  
        const phoneErr = document.getElementById('phoneError');  
  
        const emailValid = email.includes('@') && email.toLowerCase().endsWith('.com');  
        const phoneValid = /^\d{11}$/.test(phone);  
  
        if (email.length > 0 && !emailValid) {  
            emailErr.style.display = 'block';  
        } else {  
            emailErr.style.display = 'none';  
        }  
  
        if (phone.length > 0 && !phoneValid) {  
            phoneErr.style.display = 'block';  
        } else {  
            phoneErr.style.display = 'none';  
        }  
  
        if (emailValid && phoneValid) {  
            payBtn.disabled = false;  
        } else {  
            payBtn.disabled = true;  
        }  
    }  
</script>  
  
</body>  
</html>  
