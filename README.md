<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>บันทึกกิจกรรมสาธารณะประโยชน์ - RD Review</title>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Sarabun', Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 850px;
            margin: 0 auto;
            background-color: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
        }

        /* Header */
        header {
            text-align: center;
            margin-bottom: 35px;
            padding-bottom: 25px;
            border-bottom: 3px solid #667eea;
        }

        header img {
            max-width: 150px;
            height: auto;
            margin-bottom: 15px;
        }

        header h1 {
            color: #2d3748;
            font-size: 26px;
            font-weight: 700;
            margin-bottom: 12px;
        }

        header p {
            color: #718096;
            font-size: 15px;
            margin-bottom: 8px;
        }

        .google-link {
            display: inline-block;
            margin-top: 12px;
            color: #667eea;
            text-decoration: none;
            font-size: 15px;
            font-weight: 500;
            transition: color 0.3s;
        }

        .google-link:hover {
            color: #764ba2;
            text-decoration: underline;
        }

        /* Form Section */
        .form-section {
            margin-bottom: 30px;
        }

        .form-section h2 {
            color: #2d3748;
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 20px;
            padding-bottom: 12px;
            border-bottom: 2px solid #e2e8f0;
            display: flex;
            align-items: center;
        }

        .form-section h2::before {
            content: "✅";
            margin-right: 10px;
            font-size: 22px;
        }

        .form-group {
            margin-bottom: 22px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #4a5568;
            font-weight: 500;
            font-size: 15px;
        }

        input[type="text"],
        input[type="date"],
        input[type="file"],
        select,
        textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            font-size: 15px;
            font-family: 'Sarabun', Arial, sans-serif;
            transition: all 0.3s;
            background-color: #f7fafc;
        }

        input:focus,
        select:focus,
        textarea:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
            background-color: white;
        }

        textarea {
            resize: vertical;
            min-height: 120px;
        }

        select {
            cursor: pointer;
            appearance: none;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='12' viewBox='0 0 12 12'%3E%3Cpath fill='%234a5568' d='M6 9L1 4h10z'/%3E%3C/svg%3E");
            background-repeat: no-repeat;
            background-position: right 15px center;
            padding-right: 40px;
        }

        .checkbox-group {
            margin: 10px 0;
        }

        .checkbox-group label {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            font-weight: normal;
            cursor: pointer;
            padding: 10px;
            border-radius: 6px;
            transition: background-color 0.2s;
        }

        .checkbox-group label:hover {
            background-color: #f7fafc;
        }

        .checkbox-group input[type="checkbox"] {
            margin-right: 12px;
            width: 20px;
            height: 20px;
            cursor: pointer;
        }

        .required {
            color: #e53e3e;
            margin-left: 3px;
            font-weight: 700;
        }

        /* Submit Button */
        .submit-section {
            text-align: center;
            margin-top: 35px;
        }

        button[type="submit"] {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 50px;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        button[type="submit"]:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(102, 126, 234, 0.6);
        }

        button[type="submit"]:active {
            transform: translateY(0);
        }

        /* Footer */
        footer {
            margin-top: 40px;
            padding-top: 25px;
            border-top: 3px solid #667eea;
            text-align: center;
            color: #718096;
            font-size: 14px;
        }

        footer p {
            margin-bottom: 10px;
        }

        footer strong {
            color: #2d3748;
        }

        .design-notes {
            margin-top: 25px;
            padding: 20px;
            background-color: #f7fafc;
            border-radius: 8px;
            text-align: left;
        }

        .design-notes ul {
            list-style: none;
            padding: 0;
            margin-top: 15px;
        }

        .design-notes li {
            padding: 8px 0;
            color: #4a5568;
            font-size: 13px;
        }

        .design-notes li::before {
            content: "✅ ";
            color: #48bb78;
            font-weight: bold;
            margin-right: 8px;
        }

        /* Alert Overlay */
        .alert-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .alert-box {
            background: white;
            padding: 30px;
            border-radius: 12px;
            text-align: center;
            max-width: 400px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            animation: slideIn 0.3s ease-out;
        }

        @keyframes slideIn {
            from {
                transform: translateY(-50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .alert-icon {
            font-size: 60px;
            margin-bottom: 15px;
        }

        .alert-title {
            font-size: 24px;
            font-weight: 600;
            color: #2d3748;
            margin-bottom: 10px;
        }

        .alert-message {
            font-size: 16px;
            color: #718096;
            margin-bottom: 20px;
        }

        .alert-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px 40px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        .alert-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 25px;
            }

            header h1 {
                font-size: 22px;
            }

            .form-section h2 {
                font-size: 18px;
            }

            button[type="submit"] {
                padding: 12px 40px;
                font-size: 16px;
            }
        }

        @media (max-width: 480px) {
            body {
                padding: 10px;
            }

            .container {
                padding: 20px;
            }

            header img {
                max-width: 120px;
            }

            header h1 {
                font-size: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header>
            <img src="https://www.ro.ac.th/home/wp-content/uploads/2021/10/logo_RO-removebg-preview.png" alt="ตราโรงเรียนวัดราชโอรส">
            <h1>บันทึกกิจกรรมสาธารณะประโยชน์</h1>
            <p>ใช้สำหรับบันทึกกิจกรรมสาธารณะประโยชน์แบบ minimal + professional</p>
            <p>ให้ผลลัพธ์บันทึกเข้า Google Sheets โดยอัตโนมัติ</p>
            <a href="#" class="google-link">ใช้งานผ่าน Google "Prompt" คำนำ</a>
        </header>

        <!-- Form -->
        <form id="appointmentForm">
            <!-- แบบฟอร์มกรอกข้อมูลครูและรอบคัดสรร -->
            <div class="form-section">
                <h2>แบบฟอร์มกรอกข้อมูลครูและรอบคัดสรร</h2>
                
                <div class="form-group">
                    <label for="teacherName">ชื่อครู - นามสกุล <span class="required">*</span></label>
                    <input type="text" id="teacherName" name="teacherName" placeholder="กรุณากรอกชื่อ-นามสกุล" required>
                </div>

                <div class="form-group">
                    <label for="school">รหัสนักเรียน <span class="required">*</span></label>
                    <input type="text" id="school" name="school" placeholder="กรุณากรอกรหัสนักเรียน" required>
                </div>

                <div class="form-group">
                    <label for="round">รอบ <span class="required">*</span></label>
                    <select id="round" name="round" required>
                        <option value="">-- กรุณาเลือกรอบ --</option>
                        <option value="รอบ 1-13">รอบ 1-13</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="appointmentDate">วันที่ทำกิจกรรม <span class="required">*</span></label>
                    <input type="date" id="appointmentDate" name="appointmentDate" required>
                </div>

                <div class="form-group">
                    <label for="imageUpload">ช่องสำหรับแนบภาพประกอบ <span class="required">*</span></label>
                    <input type="file" id="imageUpload" name="imageUpload" accept="image/*" style="padding: 10px;" required>
                    <small style="display: block; margin-top: 5px; color: #718096;">รองรับไฟล์: JPG, PNG, GIF (ขนาดไม่เกิน 5MB)</small>
                </div>

                <div class="form-group">
                    <label for="notes">รายละเอียดความดี <span class="required">*</span></label>
                    <textarea id="notes" name="notes" placeholder="กรุณากรอกรายละเอียดความดี" required></textarea>
                </div>

                <div class="form-group">
                    <label>สอบถามคาบเรียน: เพิ่ม 10 ครบแล้ว (ให้ปรับส่อบคาบทำวิธีการ 5 ครั้ง ได้ไม่เกิน 2 คาบสอน) <span class="required">*</span></label>
                    <div class="checkbox-group">
                        <label>
                            <input type="checkbox" name="classComplete" value="ครบแล้วให้">
                            ครบแล้วให้ (fax)
                        </label>
                    </div>
                </div>
            </div>

            <!-- ปุ่มส่งข้อมูล -->
            <div class="form-section">
                <h2>ปุ่มส่งข้อมูล</h2>
                
                <div class="form-group">
                    <p style="color: #4a5568; font-size: 15px;">ปุ่มส่ง: ชื่อความ "ยืนยัน"</p>
                </div>

                <div class="form-group checkbox-group">
                    <label>
                        <input type="checkbox" name="sweetAlert" value="yes" checked>
                        เปิดหน้าเสร็จแอพเรียบร้อยแบบรับเข้น (SweetAlert style): "✅ส่งข้อมูลแล้วครับ~"
                    </label>
                </div>

                <div class="form-group">
                    <p style="color: #4a5568; font-size: 14px;">ให้ข้อมูลครอบครัวนั้นไปกำไว้ Google Sheets id = "" (เขาไปดักกำจัด)</p>
                </div>
            </div>

            <!-- Submit Button -->
            <div class="submit-section">
                <button type="submit">ยืนยัน</button>
            </div>
        </form>

        <!-- Footer -->
        <footer>
            <p><strong>แสดงข้อความกากรวการ:</strong></p>
            <p>© 2025 KKClassVIP.com ระบบนัดทันใจสมัยใหม่สำหรับ โดย ครูยอด</p>
            <p>ใช้งานรวยแฉน สร้างครัวมานะเลข</p>
            
            <div class="design-notes">
                <p style="text-align: center; font-weight: 600; color: #2d3748; margin-bottom: 10px;">
                    <strong>แนวทางออกแบบ:</strong>
                </p>
                <ul>
                    <li>ใช้ Tailwind CSS หลักเป็นรองรับส modern responsive</li>
                    <li>ทุกองค์ประกอบรวบรวมครบตัวสดุออกช้มินมัดใส่ทั้งทีเพียงแค่ใช้งานง่าย</li>
                    <li>ข้อมูลเต็มเข้ารับการบันทึกแล้วมี padding และระยะห่างทันที</li>
                    <li>อิกอนเปลาสี(พาทริเส่ครอบทรานิ่ม เเบบหน้ามาทุกที่</li>
                    <li>สร้างให้แพลจอล่าง 1ใช้ ได้ icon วิดีโอ / อักการจำกัด</li>
                    <li>Layout ชัดเจร ไม่รก</li>
                    <li>รองรับ Responsive</li>
                </ul>
            </div>
        </footer>
    </div>

    <!-- Custom Alert Overlay -->
    <div class="alert-overlay" id="alertOverlay">
        <div class="alert-box">
            <div class="alert-icon">✅</div>
            <div class="alert-title">สำเร็จ!</div>
            <div class="alert-message">ส่งข้อมูลแล้วครับ~</div>
            <button class="alert-button" onclick="closeAlert()">ตกลง</button>
        </div>
    </div>

    <script>
        // Form submission handler
        document.getElementById('appointmentForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form data
            const formData = new FormData(this);
            const data = {};
            
            // Convert FormData to object
            for (let [key, value] of formData.entries()) {
                if (data[key]) {
                    if (Array.isArray(data[key])) {
                        data[key].push(value);
                    } else {
                        data[key] = [data[key], value];
                    }
                } else {
                    data[key] = value;
                }
            }
            
            console.log('Form Data:', data);
            
            // Check if SweetAlert style is enabled
            const useSweetAlert = document.querySelector('input[name="sweetAlert"]').checked;
            
            if (useSweetAlert) {
                // Show custom alert
                showAlert();
            } else {
                alert('ส่งข้อมูลเรียบร้อยแล้ว');
                this.reset();
            }
            
            // Example: Send to Google Sheets (uncomment and configure)
            // sendToGoogleSheets(data);
        });

        function showAlert() {
            const overlay = document.getElementById('alertOverlay');
            overlay.style.display = 'flex';
        }

        function closeAlert() {
            const overlay = document.getElementById('alertOverlay');
            overlay.style.display = 'none';
            document.getElementById('appointmentForm').reset();
        }

        // Close alert when clicking outside the box
        document.getElementById('alertOverlay').addEventListener('click', function(e) {
            if (e.target === this) {
                closeAlert();
            }
        });

        // Example function to send data to Google Sheets
        // Step 1: Create a Google Apps Script Web App
        // Step 2: Deploy as web app and get the URL
        // Step 3: Replace YOUR_SCRIPT_URL below with your actual URL
        
        /*
        function sendToGoogleSheets(data) {
            const SCRIPT_URL = 'YOUR_GOOGLE_APPS_SCRIPT_URL_HERE';
            
            fetch(SCRIPT_URL, {
                method: 'POST',
                mode: 'no-cors',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify(data)
            })
            .then(response => {
                console.log('Data sent to Google Sheets successfully');
            })
            .catch(error => {
                console.error('Error sending data:', error);
            });
        }
        */

        // Google Apps Script code (to be placed in your Google Sheets script editor):
        /*
        function doPost(e) {
            var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
            var data = JSON.parse(e.postData.contents);
            
            sheet.appendRow([
                new Date(),
                data.teacherName,
                data.school,
                data.round,
                data.appointmentDate,
                data.description,
                data.notes,
                data.classComplete || 'ไม่ได้เลือก'
            ]);
            
            return ContentService.createTextOutput(JSON.stringify({result: 'success'}))
                .setMimeType(ContentService.MimeType.JSON);
        }
        */
    </script>
</body>
</html>
