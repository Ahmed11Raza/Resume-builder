# Resume-builder
## I create this resume builder for the very first time by using Typescript,HTML and CSS

%%html
<!DOCTYPE html>
<html>
<head>
  <title>Resume Builder</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    .container {
      width: 80%;
      margin: 0 auto;
      padding: 20px;
    }

    h1 {
      text-align: center;
    }

    .form-group {
      margin-bottom: 15px;
    }

    label {
      display: block;
      margin-bottom: 5px;
    }

    input[type="text"],
    textarea {
      width: 100%;
      padding: 15px;
      border: 1px solid #ccc;
      box-sizing: border-box;
    }

    button {
      background-color: #4CAF50;
      color: white;
      padding: 10px 35px;
      border: none;
      cursor: pointer;
    }

    .resume {
      margin-top: 40px;
      border: 1px solid #ccc;
      padding: 35px;
    }

    .section {
      margin-bottom: 30px;
    }

    .section-title {
      font-weight: bold;
      margin-bottom: 10px;
    }
  </style>
</head>


### <body>
  <div class="container">
    <h1>Resume Builder</h1>
    <div class="form-group">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name">
    </div>
    <div class="form-group">
      <label for="email">Email:</label>
      <input type="text" id="email" name="email">
    </div>
    <div class="form-group">
      <label for="phone">Phone:</label>
      <input type="text" id="phone" name="phone">
    </div>
    <div class="form-group">
      <label for="summary">Summary:</label>
      <textarea id="summary" name="summary"></textarea>
    </div>
    <div class="form-group">
      <label for="experience">Experience:</label>
      <textarea id="experience" name="experience"></textarea>
    </div>
    <div class="form-group">
      <label for="education">Education:</label>
      <textarea id="education" name="education"></textarea>
    </div>
    <div class="form-group">
      <label for="skills">Skills:</label>
      <textarea id="skills" name="skills"></textarea>
    </div>
    <button onclick="buildResume()">Build Resume</button>
    <div class="resume" id="resume">
    </div>
  </div>

  ### <script>
    function buildResume() {
      const name = document.getElementById("name").value;
      const email = document.getElementById("email").value;
      const phone = document.getElementById("phone").value;
      const summary = document.getElementById("summary").value;
      const experience = document.getElementById("experience").value;
      const education = document.getElementById("education").value;
      const skills = document.getElementById("skills").value;

      const resume = document.getElementById("resume");
      resume.innerHTML = "";

      const nameElement = document.createElement("h2");
      nameElement.textContent = name;
      resume.appendChild(nameElement);

      const contactElement = document.createElement("p");
      contactElement.textContent = "Email: " + email + " | Phone: " + phone;
      resume.appendChild(contactElement);

      const summaryElement = document.createElement("div");
      summaryElement.classList.add("section");
      const summaryTitle = document.createElement("h3");
      summaryTitle.classList.add("section-title");
      summaryTitle.textContent = "Summary";
      summaryElement.appendChild(summaryTitle);
      const summaryContent = document.createElement("p");
      summaryContent.textContent = summary;
      summaryElement.appendChild(summaryContent);
      resume.appendChild(summaryElement);

      const experienceElement = document.createElement("div");
      experienceElement.classList.add("section");
      const experienceTitle = document.createElement("h3");
      experienceTitle.classList.add("section-title");
      experienceTitle.textContent = "Experience";
      experienceElement.appendChild(experienceTitle);
      const experienceContent = document.createElement("p");
      experienceContent.textContent = experience;
      experienceElement.appendChild(experienceContent);
      resume.appendChild(experienceElement);

      const educationElement = document.createElement("div");
      educationElement.classList.add("section");
      const educationTitle = document.createElement("h3");
      educationTitle.classList.add("section-title");
      educationTitle.textContent = "Education";
      educationElement.appendChild(educationTitle);
      const educationContent = document.createElement("p");
      educationContent.textContent = education;
      educationElement.appendChild(educationContent);
      resume.appendChild(educationElement);

      const skillsElement = document.createElement("div");
      skillsElement.classList.add("section");
      const skillsTitle = document.createElement("h3");
      skillsTitle.classList.add("section-title");
      skillsTitle.textContent = "Skills";
      skillsElement.appendChild(skillsTitle);
      const skillsContent = document.createElement("p");
      skillsContent.textContent = skills;
      skillsElement.appendChild(skillsContent);
      resume.appendChild(skillsElement);
    }
  </script>
</body>
</html>
