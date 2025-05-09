<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>个人简历表单</title>
    <style>
        body {
            font-family: 'Microsoft YaHei', sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            color: #333;
            background-color: #f5f5f5;
        }
        .form-title {
            text-align: center;
            font-size: 24px;
            margin-bottom: 20px;
            color: #2c3e50;
            font-weight: bold;
        }
        fieldset {
            border: 2px solid #3498db;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 20px;
            background-color: white;
        }
        legend {
            font-size: 18px;
            font-weight: bold;
            color: #3498db;
            padding: 0 10px;
        }
        .resume-table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        .resume-table th, .resume-table td {
            border: 1px solid #ddd;
            padding: 12px 15px;
            text-align: left;
        }
        .resume-table th {
            background-color: #f2f2f2;
            width: 15%;
        }
        .photo-cell {
            text-align: center;
            width: 100px;
        }
        .resume-photo {
            width: 100px;
            height: 130px;
            object-fit: cover;
            border: 1px solid #ddd;
        }
        input[type="text"],
        input[type="tel"],
        input[type="email"],
        input[type="number"],
        select,
        textarea {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        textarea {
            height: 100px;
            resize: vertical;
        }
        .radio-group, .checkbox-group {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        button {
            background-color: #3498db;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            display: block;
            margin: 20px auto;
        }
        button:hover {
            background-color: #2980b9;
        }
        .section-title {
            font-size: 18px;
            margin: 15px 0;
            padding-bottom: 5px;
            border-bottom: 2px solid #3498db;
            color: #2c3e50;
        }
        .content-block {
            margin-bottom: 15px;
        }
    </style>
</head>
<body>
    <div class="form-title">个人简历表单</div>

    <form action="#" method="post" enctype="multipart/form-data">
        <fieldset>
            <legend>基本信息</legend>
            <table class="resume-table">
                <tr>
                    <th><label for="fullname">姓名</label></th>
                    <td><input type="text" id="fullname" name="fullname" required maxlength="20"></td>
                    <th><label>性别</label></th>
                    <td>
                        <div class="radio-group">
                            <label><input type="radio" name="gender" value="male" checked> 男</label>
                            <label><input type="radio" name="gender" value="female"> 女</label>
                        </div>
                    </td>
                    <th rowspan="4">照片</th>
                    <td rowspan="4" class="photo-cell">
                        <input type="file" id="photo" name="photo" accept="image/*" required>
                    </td>
                </tr>
                <tr>
                    <th><label for="age">年龄</label></th>
                    <td><input type="number" id="age" name="age" min="18" max="60" required></td>
                    <th><label for="hometown">籍贯</label></th>
                    <td><input type="text" id="hometown" name="hometown" required maxlength="20"></td>
                </tr>
                <tr>
                    <th><label for="phone">联系电话</label></th>
                    <td><input type="tel" id="phone" name="phone" required maxlength="11" pattern="\d{11}"></td>
                    <th><label for="email">电子邮箱</label></th>
                    <td><input type="email" id="email" name="email" required maxlength="50"></td>
                </tr>
                <tr>
                    <th><label for="education">学历</label></th>
                    <td>
                        <select id="education" name="education" required>
                            <option value="">请选择</option>
                            <option value="highschool">高中及以下</option>
                            <option value="college">大专</option>
                            <option value="bachelor">本科</option>
                            <option value="master">硕士</option>
                            <option value="phd">博士</option>
                        </select>
                    </td>
                    <th><label for="marital">婚姻状况</label></th>
                    <td>
                        <select id="marital" name="marital" required>
                            <option value="">请选择</option>
                            <option value="single">未婚</option>
                            <option value="married">已婚</option>
                            <option value="divorced">离异</option>
                        </select>
                    </td>
                </tr>
                <tr>
                    <th><label for="health">健康状况</label></th>
                    <td>
                        <select id="health" name="health" required>
                            <option value="">请选择</option>
                            <option value="excellent">优秀</option>
                            <option value="good">良好</option>
                            <option value="fair">一般</option>
                        </select>
                    </td>
                    <th><label for="job_target">求职意向</label></th>
                    <td colspan="3"><input type="text" id="job_target" name="job_target" required maxlength="50"></td>
                </tr>
                <tr>
                    <th><label for="major">专业</label></th>
                    <td><input type="text" id="major" name="major" required maxlength="30"></td>
                    <th><label for="school">毕业院校</label></th>
                    <td colspan="3"><input type="text" id="school" name="school" required maxlength="50"></td>
                </tr>
            </table>
        </fieldset>

        <fieldset>
            <legend>详细信息</legend>
            <div class="section-title">技能证书</div>
            <div class="content-block">
                <textarea id="certificates" name="certificates" placeholder="请输入您的技能证书信息，每项用逗号或分号分隔" maxlength="500"></textarea>
            </div>

            <div class="section-title">个人特长与爱好</div>
            <div class="content-block">
                <textarea id="hobbies" name="hobbies" placeholder="请输入您的特长与爱好，每项用逗号或分号分隔" maxlength="300"></textarea>
            </div>

            <div class="section-title">项目经历</div>
            <div class="content-block">
                <textarea id="projects" name="projects" placeholder="请按以下格式填写项目经历：&#10;项目名称(时间): 项目描述&#10;• 职责1&#10;• 职责2" maxlength="1000"></textarea>
            </div>

            <div class="section-title">自我评价</div>
            <div class="content-block">
                <textarea id="self_evaluation" name="self_evaluation" placeholder="请简要描述您的自我评价" maxlength="800"></textarea>
            </div>

            <div class="section-title">其他信息</div>
            <div class="content-block">
                <label><input type="checkbox" name="agree" required> 我确认以上信息真实有效</label>
            </div>
        </fieldset>

        <button type="submit">提交简历</button>
    </form>
</body>
</html>
