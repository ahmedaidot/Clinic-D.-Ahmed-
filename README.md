<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>عيادة د. أحمد عباس لطب الأسنان</title>
  <!-- Font Awesome 6 (الأيقونات الطبية) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Google Fonts: خط عربي حديث (تاجوال) -->
  <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Tajawal', sans-serif;
      background-color: #ffffff;
      color: #1e2b37;
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    /* الألوان الأساسية: أبيض، أزرق هادئ، فضي */
    :root {
      --primary-blue: #4a90e2;        /* أزرق هادئ */
      --light-blue: #e6f2ff;           /* خلفية زرقاء فاتحة جداً */
      --silver: #f4f7fb;               /* فضي ناعم */
      --dark-silver: #e0e7ef;
      --text-dark: #1e2b37;
      --text-soft: #3a4a5a;
      --white: #ffffff;
      --shadow: 0 8px 20px rgba(0, 40, 80, 0.06);
      --border-radius: 20px;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 1.5rem 0;
    }

    /* العناوين والمسافات */
    section {
      padding: 3rem 0;
    }

    h1, h2, h3 {
      font-weight: 700;
      color: var(--text-dark);
      letter-spacing: -0.01em;
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 2rem;
      position: relative;
      display: inline-block;
    }
    h2:after {
      content: '';
      display: block;
      width: 60%;
      height: 4px;
      background: linear-gradient(90deg, var(--primary-blue), transparent);
      border-radius: 4px;
      margin-top: 8px;
    }

    /* الأزرار */
    .btn {
      display: inline-block;
      background: var(--primary-blue);
      color: white;
      padding: 0.9rem 2rem;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      font-size: 1.1rem;
      border: none;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 6px 14px rgba(74, 144, 226, 0.25);
    }
    .btn-outline {
      background: transparent;
      color: var(--primary-blue);
      border: 2px solid var(--primary-blue);
      box-shadow: none;
    }
    .btn-outline:hover {
      background: var(--primary-blue);
      color: white;
      transform: translateY(-3px);
    }
    .btn:hover {
      background: #2670c2;
      transform: translateY(-3px);
      box-shadow: 0 12px 22px rgba(74, 144, 226, 0.35);
    }

    /* بطاقات وخدمات */
    .card {
      background: var(--white);
      border-radius: var(--border-radius);
      padding: 2rem 1.5rem;
      box-shadow: var(--shadow);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      border: 1px solid rgba(224, 231, 239, 0.5);
      backdrop-filter: blur(2px);
      text-align: center;
    }
    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 30px rgba(0, 50, 90, 0.1);
      border-color: var(--primary-blue);
    }
    .card i {
      font-size: 3rem;
      color: var(--primary-blue);
      margin-bottom: 1rem;
      background: var(--light-blue);
      width: 80px;
      height: 80px;
      line-height: 80px !important;
      border-radius: 50%;
      text-align: center;
      display: inline-block;
    }

    /* شبكات */
    .grid-2, .grid-4 {
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    @media (min-width: 640px) {
      .grid-2 {
        grid-template-columns: repeat(2, 1fr);
      }
      .grid-4 {
        grid-template-columns: repeat(2, 1fr);
      }
    }
    @media (min-width: 992px) {
      .grid-4 {
        grid-template-columns: repeat(4, 1fr);
      }
    }

    /* ترويسة خفيفة */
    .clinic-name {
      font-size: 1.6rem;
      font-weight: 700;
      color: var(--primary-blue);
      padding: 1rem 0;
      border-bottom: 1px solid var(--dark-silver);
    }
    .clinic-name i {
      margin-left: 0.6rem;
      color: var(--primary-blue);
    }

    /* قسم الترحيب */
    .hero {
      background: linear-gradient(145deg, var(--silver) 0%, #ffffff 80%);
      border-radius: 0 0 var(--border-radius) var(--border-radius);
    }
    .hero-content {
      display: flex;
      flex-direction: column;
      gap: 2rem;
    }
    .hero-text h1 {
      font-size: 2.6rem;
      line-height: 1.3;
      margin-bottom: 1.2rem;
    }
    .hero-text p {
      font-size: 1.3rem;
      color: var(--text-soft);
      margin-bottom: 2rem;
    }
    .hero-buttons {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    /* نموذج الحجز */
    .booking-form {
      background: var(--silver);
      border-radius: var(--border-radius);
      padding: 2.5rem;
      margin-top: 2rem;
    }
    .form-group {
      margin-bottom: 1.5rem;
    }
    label {
      display: block;
      font-weight: 600;
      margin-bottom: 0.5rem;
      color: var(--text-dark);
    }
    input, select, textarea {
      width: 100%;
      padding: 1rem 1.2rem;
      border: 1px solid var(--dark-silver);
      border-radius: 60px;
      font-family: 'Tajawal', sans-serif;
      font-size: 1rem;
      background: var(--white);
      transition: 0.2s;
    }
    input:focus, select:focus, textarea:focus {
      outline: none;
      border-color: var(--primary-blue);
      box-shadow: 0 0 0 4px rgba(74, 144, 226, 0.15);
    }
    textarea {
      border-radius: 30px;
      resize: vertical;
    }
    .time-select {
      background: white;
    }
    option:disabled {
      background: #f0f0f0;
      color: #aaa;
    }

    /* قسم الموقع */
    .map-card {
      background: var(--silver);
      border-radius: var(--border-radius);
      padding: 2rem;
      text-align: center;
      border: 1px solid var(--dark-silver);
    }
    .map-card .btn {
      margin-top: 1rem;
    }
    .whatsapp-number {
      direction: ltr;
      display: inline-block;
      background: white;
      padding: 0.6rem 1.5rem;
      border-radius: 40px;
      font-weight: 600;
      color: #25D366;
      border: 1px solid #25D366;
    }

    /* why us */
    .feature-item {
      display: flex;
      align-items: center;
      gap: 1rem;
      background: white;
      padding: 1.2rem;
      border-radius: 50px;
      box-shadow: var(--shadow);
      margin-bottom: 1rem;
    }
    .feature-item i {
      font-size: 2rem;
      color: var(--primary-blue);
      background: var(--light-blue);
      border-radius: 50%;
      width: 60px;
      height: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    /* تذييل */
    footer {
      background: var(--text-dark);
      color: white;
      text-align: center;
      padding: 2rem;
      margin-top: 3rem;
      border-radius: 40px 40px 0 0;
    }

    /* رسالة نجاح */
    .success-toast {
      background: #27ae60;
      color: white;
      padding: 1rem 2rem;
      border-radius: 60px;
      position: fixed;
      bottom: 20px;
      left: 20px;
      right: 20px;
      max-width: 400px;
      margin: 0 auto;
      text-align: center;
      font-weight: 700;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      z-index: 1000;
      display: none;
    }
    .success-toast.show {
      display: block;
      animation: slideUp 0.3s ease;
    }
    @keyframes slideUp {
      from { transform: translateY(30px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
  </style>
</head>
<body>
  <!-- شريط اسم العيادة -->
  <div class="container">
    <div class="clinic-name">
      <i class="fas fa-tooth"></i> عيادة د. أحمد عباس لطب الأسنان
    </div>
  </div>

  <!-- قسم الترحيب -->
  <section class="hero">
    <div class="container hero-content">
      <div class="hero-text">
        <h1>ابتسامتك تبدأ من هنا</h1>
        <p>عناية فائقة بأسنانك بأحدث التقنيات في بيئة مريحة ومعقمة. فريقنا المتخصص يضمن لك أفضل النتائج.</p>
        <div class="hero-buttons">
          <a href="#booking" class="btn"><i class="fas fa-calendar-check"></i> احجز موعد</a>
          <a href="https://wa.me/9647750763403" target="_blank" class="btn btn-outline"><i class="fab fa-whatsapp"></i> تواصل واتساب</a>
        </div>
      </div>
      <div class="hero-image">
        <!-- يمكن إضافة صورة توضيحية، لكن نكتفي بالنص النظيف -->
      </div>
    </div>
  </section>

  <!-- قسم الخدمات -->
  <section id="services">
    <div class="container">
      <h2><i class="fas fa-briefcase-medical"></i> خدماتنا</h2>
      <div class="grid-4">
        <div class="card">
          <i class="fas fa-brush"></i>
          <h3>تنظيف الأسنان وإزالة التكلسات والجير</h3>
        </div>
        <div class="card">
          <i class="fas fa-lightbulb"></i>
          <h3>حشوات ضوئية دائمية مدفوعة</h3>
        </div>
        <div class="card">
          <i class="fas fa-teeth"></i>
          <h3>تركيب أطقم الأسنان</h3>
        </div>
        <div class="card">
          <i class="fas fa-tooth"></i>
          <h3>إزالة الأسنان التالفة والمكسورة</h3>
        </div>
      </div>
    </div>
  </section>

  <!-- لماذا تختارنا -->
  <section style="background-color: var(--silver);">
    <div class="container">
      <h2><i class="fas fa-star"></i> لماذا تختارنا</h2>
      <div class="grid-2">
        <div class="feature-item"><i class="fas fa-bullseye"></i> دقة عالية في العلاج</div>
        <div class="feature-item"><i class="fas fa-microscope"></i> أجهزة حديثة</div>
        <div class="feature-item"><i class="fas fa-user-md"></i> راحة المريض</div>
        <div class="feature-item"><i class="fas fa-hand-holding-heart"></i> تعقيم احترافي</div>
      </div>
    </div>
  </section>

  <!-- قسم الحجز (النموذج الذكي) -->
  <section id="booking">
    <div class="container">
      <h2><i class="fas fa-calendar-alt"></i> حجز موعد</h2>
      <div class="booking-form" id="bookingFormContainer">
        <form id="appointmentForm">
          <div class="form-group">
            <label>الاسم الكامل <span style="color:var(--primary-blue);">*</span></label>
            <input type="text" id="fullName" placeholder="أدخل اسمك الكامل" required>
          </div>
          <div class="form-group">
            <label>رقم الهاتف <span style="color:var(--primary-blue);">*</span></label>
            <input type="tel" id="phone" placeholder="مثال: 9647750763403" required>
          </div>
          <div class="form-group">
            <label>الخدمة المطلوبة</label>
            <select id="service">
              <option value="تنظيف الأسنان وإزالة التكلسات">تنظيف الأسنان وإزالة التكلسات والجير</option>
              <option value="حشوات ضوئية دائمية">حشوات ضوئية دائمية مدفوعة</option>
              <option value="تركيب أطقم الأسنان">تركيب أطقم الأسنان</option>
              <option value="إزالة أسنان تالفة">إزالة الأسنان التالفة والمكسورة</option>
            </select>
          </div>
          <div class="form-group">
            <label>اختر التاريخ</label>
            <input type="date" id="appointmentDate" required>
          </div>
          <div class="form-group">
            <label>اختر الوقت</label>
            <select id="appointmentTime" required>
              <option value="">-- اختر الوقت --</option>
            </select>
          </div>
          <div class="form-group">
            <label>ملاحظات إضافية</label>
            <textarea id="notes" rows="3" placeholder="أي تفاصيل أخرى..."></textarea>
          </div>
          <button type="submit" class="btn" style="width: 100%;"><i class="fas fa-check-circle"></i> تأكيد الحجز</button>
        </form>
      </div>
    </div>
  </section>

  <!-- قسم الموقع والتواصل -->
  <section style="background-color: var(--light-blue);">
    <div class="container">
      <h2><i class="fas fa-map-marker-alt"></i> موقعنا و التواصل</h2>
      <div class="grid-2">
        <div class="map-card">
          <i class="fas fa-map-marked-alt fa-3x" style="color: var(--primary-blue); margin-bottom: 1rem;"></i>
          <h3>العنوان</h3>
          <p>العراق، بغداد، شارع الربيع – مجمع الأسنان الطبي</p>
          <a href="https://maps.app.goo.gl/5duVANBeahjdTYmn9?g_st=atm" target="_blank" class="btn btn-outline" style="margin: 0.5rem 0;"><i class="fas fa-map-signs"></i> فتح الخريطة</a>
          <br>
          <small>رابط مباشر: <a href="https://maps.app.goo.gl/5duVANBeahjdTYmn9?g_st=atm" target="_blank" style="color: var(--primary-blue);">خرائط Google</a></small>
        </div>
        <div class="map-card">
          <i class="fab fa-whatsapp fa-3x" style="color:#25D366; margin-bottom: 1rem;"></i>
          <h3>تواصل عبر واتساب</h3>
          <p class="whatsapp-number">+964 775 076 3403</p>
          <a href="https://wa.me/9647750763403" target="_blank" class="btn" style="background:#25D366; color:white;"><i class="fab fa-whatsapp"></i> مراسلة فورية</a>
          <br>
          <small>رقم الحجز المباشر</small>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 عيادة د. أحمد عباس – كل الحقوق محفوظة. ابتسامتك أمانة.</p>
  </footer>

  <!-- رسالة تأكيد -->
  <div id="successToast" class="success-toast">✅ تم حجز موعدك بنجاح</div>

  <script>
    (function() {
      // --- الإعدادات الأساسية ---
      const CLINIC_WHATSAPP = '9647750763403';
      const TIME_SLOTS = [
        '09:00', '09:30', '10:00', '10:30', '11:00', '11:30', '12:00', '12:30',
        '13:00', '13:30', '14:00', '14:30', '15:00', '15:30', '16:00', '16:30', '17:00'
      ];

      // --- إدارة المواعيد (localStorage) ---
      let appointments = [];

      // تحميل أو تهيئة بيانات تجريبية لمرة واحدة
      function loadAppointments() {
        const stored = localStorage.getItem('dentalAppointments');
        if (stored) {
          try {
            appointments = JSON.parse(stored);
          } catch { appointments = []; }
        } else {
          // بيانات وهمية لإظهار منع تضارب (مواعيد مستقبلية)
          const today = new Date();
          const tomorrow = new Date(today);
          tomorrow.setDate(tomorrow.getDate() + 1);
          const dayAfter = new Date(today);
          dayAfter.setDate(dayAfter.getDate() + 2);

          const fmtDate = (d) => d.toISOString().split('T')[0];
          appointments = [
            { date: fmtDate(tomorrow), time: '10:00', name: 'حسين علي', phone: '964780123456', service: 'تنظيف' },
            { date: fmtDate(dayAfter), time: '11:30', name: 'زينب محمد', phone: '964770987654', service: 'حشوة' },
          ];
          localStorage.setItem('dentalAppointments', JSON.stringify(appointments));
        }
      }
      loadAppointments();

      function saveAppointments() {
        localStorage.setItem('dentalAppointments', JSON.stringify(appointments));
      }

      // التحقق من وجود تعارض (تاريخ ووقت محددين)
      function isTimeBooked(date, time) {
        return appointments.some(apt => apt.date === date && apt.time === time);
      }

      // --- عناصر DOM ---
      const dateInput = document.getElementById('appointmentDate');
      const timeSelect = document.getElementById('appointmentTime');
      const form = document.getElementById('appointmentForm');
      const fullName = document.getElementById('fullName');
      const phone = document.getElementById('phone');
      const service = document.getElementById('service');
      const notes = document.getElementById('notes');
      const toast = document.getElementById('successToast');

      // تعيين الحد الأدنى للتاريخ (اليوم)
      const today = new Date().toISOString().split('T')[0];
      dateInput.setAttribute('min', today);

      // دالة ملء أوقات الوقت بناءً على التاريخ المختار
      function populateTimes(selectedDate) {
        // حفظ القيمة المحددة حاليًا (إن وجدت)
        const currentTime = timeSelect.value;
        timeSelect.innerHTML = '<option value="">-- اختر الوقت --</option>';

        if (!selectedDate) return;

        TIME_SLOTS.forEach(slot => {
          const option = document.createElement('option');
          option.value = slot;
          option.textContent = slot;
          if (isTimeBooked(selectedDate, slot)) {
            option.disabled = true;
            option.textContent += ' (محجوز)';
          }
          timeSelect.appendChild(option);
        });

        // استعادة القيمة إذا كانت لا تزال متاحة
        if (currentTime) {
          const stillAvailable = !isTimeBooked(selectedDate, currentTime);
          const optionExists = [...timeSelect.options].some(opt => opt.value === currentTime && !opt.disabled);
          if (stillAvailable && optionExists) {
            timeSelect.value = currentTime;
          }
        }
      }

      // عند تغيير التاريخ، أعد بناء قائمة الأوقات
      dateInput.addEventListener('change', function(e) {
        populateTimes(e.target.value);
      });

      // تحقق أولي عند تحميل الصفحة (إن كان هناك تاريخ افتراضي)
      if (dateInput.value) {
        populateTimes(dateInput.value);
      }

      // --- التحقق من صحة رقم الهاتف (أرقام فقط، + اختياري، طول 10-15)
      function validatePhone(phoneStr) {
        const re = /^[\+]?[0-9]{10,15}$/;
        return re.test(phoneStr.replace(/\s/g, ''));
      }

      // --- إرسال النموذج ---
      form.addEventListener('submit', function(e) {
        e.preventDefault();

        // جمع القيم
        const nameVal = fullName.value.trim();
        const phoneVal = phone.value.trim();
        const serviceVal = service.value;
        const dateVal = dateInput.value;
        const timeVal = timeSelect.value;
        const notesVal = notes.value.trim();

        // تحقق أساسي
        if (!nameVal) {
          alert('الرجاء إدخال الاسم الكامل');
          return;
        }
        if (!validatePhone(phoneVal)) {
          alert('رقم الهاتف غير صالح. يجب أن يتكون من 10 إلى 15 رقماً (يمكن البدء بـ +)');
          return;
        }
        if (!dateVal) {
          alert('اختر تاريخ الموعد');
          return;
        }
        if (!timeVal) {
          alert('اختر الوقت المناسب');
          return;
        }

        // التحقق من عدم حجز الوقت (مرة أخرى)
        if (isTimeBooked(dateVal, timeVal)) {
          alert('عذراً، هذا الوقت محجوز مسبقاً. الرجاء اختيار وقت آخر.');
          populateTimes(dateVal); // تحديث القائمة
          return;
        }

        // إضافة الموعد الجديد
        const newAppointment = {
          name: nameVal,
          phone: phoneVal,
          service: serviceVal,
          date: dateVal,
          time: timeVal,
          notes: notesVal,
        };
        appointments.push(newAppointment);
        saveAppointments();

        // تحديث قائمة الأوقات (لتعطيل الوقت الجديد)
        populateTimes(dateVal);

        // إرسال رسالة واتساب تلقائياً إلى العيادة
        const message = `حجز موعد جديد:
👤 اسم المريض: ${nameVal}
📞 رقم الهاتف: ${phoneVal}
🦷 الخدمة: ${serviceVal}
📅 التاريخ: ${dateVal}
⏰ الوقت: ${timeVal}
📝 ملاحظات: ${notesVal || 'لا يوجد'}`;

        const encodedMsg = encodeURIComponent(message);
        const whatsappUrl = `https://wa.me/${CLINIC_WHATSAPP}?text=${encodedMsg}`;
        window.open(whatsappUrl, '_blank');

        // عرض رسالة نجاح
        toast.classList.add('show');
        setTimeout(() => toast.classList.remove('show'), 4000);

        // إعادة تعيين الحقول (مع الاحتفاظ بالخدمة والتاريخ فارغ)
        fullName.value = '';
        phone.value = '';
        service.value = 'تنظيف الأسنان وإزالة التكلسات'; // أول قيمة
        dateInput.value = '';
        timeSelect.innerHTML = '<option value="">-- اختر الوقت --</option>';
        notes.value = '';
      });

      // جعل زر "احجز موعد" في الهيرو ينقل إلى النموذج بسلاسة
      document.querySelectorAll('a[href="#booking"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
          e.preventDefault();
          document.getElementById('booking').scrollIntoView({ behavior: 'smooth' });
        });
      });

      // إضافة بعض الأوقات المحجوزة بشكل ديناميكي (بجانب الوهمية) عند التغيير
      // تم تضمينه في populateTimes

    })();
  </script>

  <!-- إضافة بعض اللمسات البصرية: تدرج خلفية ناعم -->
  <style>
    /* تحسينات إضافية */
    .hero-text p { font-weight: 300; background: rgba(255,255,255,0.7); padding: 1rem 2rem; border-radius: 60px; display: inline-block; }
    .btn i { margin-left: 0.5rem; }
    @media (max-width: 600px) {
      h2 { font-size: 1.8rem; }
      .hero-text h1 { font-size: 2rem; }
    }
  </style>
</body>
</html>
