<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Portfolio</title>
    <link rel="stylesheet" href="style.css">
    <link
      rel="stylesheet"
      href="https://unpkg.com/boxicons@latest/css/boxicons.min.css"
    />
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet" />
  </head>
  <style>
    /* Google Font - Poppins */
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
/* Variables */
:root {
  --header-height: 3rem;
  --font-semi: 600;
}

/* Colors */

:root {
  --first-color: #4070f4;
  --second-color: #0e2431;
  --gardient-color: linear-gradient(to right, #5001fb, #8e0af3);
}

/* FONT STYLE */
:root {
  --body-font: "Poppins", sans-serif;
  --big-font-size: 2rem;
  --h2-font-size: 1.5rem;
  --nomral-font-size: 0.938rem;
}

/* Media Screen Min-Width : 768px */
@media screen and (min-width: 768px) {
  :root {
    --big-font-size: 3.5rem;
    --h2-font-size: 2rem;
    --nomral-font-size: 1rem;
  }
}

/* Margins */
:root {
  --mb-1: 0.5rem;
  --mb-2: 1rem;
  --mb-3: 1.5rem;
  --mb-4: 2rem;
  --mb-5: 2.5rem;
  --mb-6: 3rem;
}

/* Z-index */
:root {
  --z-back: -10;
  --z-normal: 1;
  --z-tooltip: 10;
  --z-fixed: 100;
}

/* Base */
*,
::before,
::before {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: var(--header-height) 0 0 0;
  font-family: var(--body-font);
  font-size: var(--nomral-font-size);
  color: var(--second-color);
}

h1,
h2,
p {
  margin: 0;
}

ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

a {
  text-decoration: none;
}

img {
  max-width: 100%;
  height: auto;
  display: block;
}

/* CUSTOM CSS CLASSES */

/* LAYOUT */
.bd_grid {
  max-width: 1024px;
  display: grid;
  grid-template-columns: 100%;
  grid-column-gap: 2rem;
  width: calc(100% - 2rem);
  margin-left: var(--mb-2);
  margin-right: var(--mb-2);
}

.header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: var(--z-fixed);
  background: #fff;
  box-shadow: 0 1px 4px rgba(146, 161, 176, 0.15);
}

/* Navbar */
.nav {
  height: var(--header-height);
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: var(--font-semi);
}

@media screen and (max-width: 768px) {
  .nav_menu {
    position: fixed;
    top: var(--header-height);
    right: -100%;
    width: 80%;
    height: 100%;
    padding: 2rem;
    background-color: var(--second-color);
    transition: 0.5s;
  }
}

.nav_items {
  margin-bottom: var(--mb-4);
}

.nav_link {
  position: relative;
  color: #fff;
}

.nav_link:hover {
  position: relative;
}

.nav_link:hover::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 0.18rem;
  left: 0;
  top: 2rem;
  background-color: var(--first-color);
}

.nav_logo {
  color: var(--second-color);
}

.nav_toggle {
  color: var(--second-color);
  font-size: 1.5rem;
  cursor: pointer;
}

/* ACTIVE MENU */
.active::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 0.18rem;
  left: 0;
  top: 2rem;
  background-color: var(--first-color);
}

.show {
  right: 0;
}

.home {
  height: calc(100vh - 3rem);
  row-gap: 1rem;
}

.home_data {
  align-self: center;
}

.home_title {
  font-size: var(--big-font-size);
  margin-bottom: var(--mb-5);
}

.home_title-color {
  color: var(--first-color);
}

.home_social {
  display: flex;
  flex-direction: column;
}

.home_social-icon {
  width: max-content;
  margin-bottom: var(--mb-2);
  font-size: 1.5rem;
  color: var(--second-color);
}

.home_social-icon:hover {
  color: var(--first-color);
}

.home_img {
  position: absolute;
  right: 0;
  bottom: 0;
  width: 300px;
}

.home_img svg {
  width: 100%;
}

/* BUTTONS */
.button {
  display: inline-block;
  color: #fff;
  padding: 0.75rem 2.5rem;
  font-weight: var(--font-semi);
  border-radius: 0.5rem;
  background: var(--gardient-color);
}

.button:hover {
  box-shadow: 0 10px 36px rgba(0, 0, 0, 0.15);
}

.section {
  padding-top: 3rem;
  padding-bottom: 2rem;
}

.section-title {
  position: relative;
  font-size: var(--h2-font-size);
  color: var(--first-color);
  margin-top: var(--mb-2);
  margin-bottom: var(--mb-4);
  text-align: center;
}

.section-title::after {
  position: absolute;
  content: "";
  width: 64px;
  height: 0.18rem;
  left: 0;
  right: 0;
  margin: auto;
  top: 2rem;
  background-color: var(--first-color);
}

/* ABOUT SECTION */

.about_container {
  row-gap: 2rem;
  text-align: center;
}

.about_subtitle {
  margin-bottom: var(--mb-2);
}

.about_img {
  justify-content: center;
}

.about_img svg {
  width: 300px;
  border-radius: 0.5rem;
}

/* SKILLS */
.skills_container {
  row-gap: 2rem;
  text-align: center;
}

.skills_subtitle {
  margin-bottom: var(--mb-2);
}

.skills_text {
  margin-bottom: var(--mb-4);
}

.skills_data {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  font-weight: var(--font-semi);
  padding: 0.5rem 1rem;
  margin-bottom: var(--mb-4);
  border-radius: 0.5rem;
  box-shadow: 0 4px 25px rgba(14, 36, 49, 0.15);
}

.skill_icon {
  font-size: 2rem;
  margin-right: var(--mb-2);
  color: var(--first-color);
}

.skills_name {
  display: flex;
  align-items: center;
}

.skill_bar {
  position: absolute;
  left: 0;
  bottom: 0;
  background-color: var(--first-color);
  height: 0.25rem;
  border-radius: 0.5rem;
  z-index: var(--z-back);
}

.skill_html {
  width: 75%;
}

.skill_css {
  width: 65%;
}

.skill_js {
  width: 30%;
}

.skill_ui {
  width: 95%;
}

/* WORK */

.work {
  text-align: center;
}

.work_container {
  row-gap: 2rem;
}

.work_img {
  box-shadow: 0 4px 25px rgba(14, 36, 49, 0.15);
  border-radius: 0.5rem;
  overflow: hidden;
}

.work_img img {
  transition: 1s;
  cursor: pointer;
}

.work_img img:hover {
  transform: scale(1.1);
}

/* Contact */

.control_input {
  width: 100%;
  font-size: var(--nomral-font-size);
  font-weight: var(--font-semi);
  padding: 1rem;
  border-radius: 0.5rem;
  border: 1.5px solid var(--second-color);
  outline: none;
  margin-bottom: var(--mb-4);
}

.control_button {
  display: block;
  border: none;
  outline: none;
  font-size: var(--nomral-font-size);
  cursor: pointer;
  margin-left: auto;
}

/* Footer */
.footer {
  background-color: var(--second-color);
  color: #fff;
  text-align: center;
  font-weight: var(--font-semi);
  padding: 2rem 0;
}

.footer_title {
  font-size: 2rem;
  margin-bottom: var(--mb-4);
}

.footer_socials {
  margin-bottom: var(--mb-4);
}

.footer_icon {
  font-size: 1.5rem;
  color: #fff;
  margin: 0 var(--mb-2);
}

@media screen and (min-width: 768px) {
  body {
    margin: 0;
  }

  .section {
    padding-top: 4rem;
    padding-bottom: 3rem;
  }
  .section-title {
    margin-bottom: var(--mb-6);
  }

  .section-title::after {
    width: 80px;
    top: 3rem;
  }

  .nav {
    height: calc(var(--header-height) + 1rem);
  }

  .nav_items {
    margin-left: var(--mb-6);
    margin-bottom: 0;
  }

  .nav_list {
    display: flex;
    padding-top: 0;
  }

  .nav_toggle {
    display: none;
  }

  .nav_link {
    color: var(--second-color);
  }

  .home {
    height: 100vh;
  }

  .home_data {
    align-self: flex-end;
  }
  .home_social {
    padding-top: 0;
    padding-bottom: 2.5rem;
    flex-direction: row;
    align-self: flex-end;
  }

  .home_social-icon {
    margin-bottom: 0;
    margin-right: var(--mb-4);
  }

  .home_img {
    width: 460px;
    bottom: 15%;
  }

  .home_img svg {
    width: 100%;
  }

  .about_container,
  .skills_container {
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
    text-align: initial;
  }

  .about_img svg {
    width: 450px;
  }

  .work_container {
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    column-gap: 2rem;
  }

  .contact_form {
    width: 400px;
  }
  .contact_container {
    justify-items: center;
  }
}

@media screen and (min-width: 1024px) {
  .bd_grid {
    margin-left: auto;
    margin-right: auto;
  }

  .home_img {
    right: 10%;
  }
}
  </style>
  <body>
    <!-- Header Section -->
    <header class="header">
      <nav class="nav bd_grid">
        <div>
          <a href="#" class="nav_logo">Shiny Sandhya</a>
        </div>

        <div class="nav_menu" id="nav_menu">
          <ul class="nav_list">
            <li class="nav_items">
              <a href="#home" class="nav_link active">Home</a>
            </li>
            <li class="nav_items">
              <a href="#about" class="nav_link active">About</a>
            </li>
            <li class="nav_items">
              <a href="#skills" class="nav_link active">Skills</a>
            </li>
            <li class="nav_items">
              <a href="#work" class="nav_link active">Work</a>
            </li>
            <li class="nav_items">
              <a href="#contact" class="nav_link active">Contact</a>
            </li>
          </ul>
        </div>

        <div class="nav_toggle" id="nav_toggle">
          <i class="bx bx-menu-alt-right"></i>
        </div>
      </nav>
    </header>

    <main class="main">
      <!-- HOME SECTION -->
      <section class="home bd_grid" id="home">
        <div class="home_data" data-aos="fade-down">
          <h1 class="home_title">
            Hi, <br />I'm <span class="home_title-color">Shiny Sandhya</span
            ><br />Student
          </h1>
          <a href="#contact" class="button"> Contact</a>
          <a href="#contact" class="button">Resume</a>
        </div>

        <div class="home_social">
          <a href="#" class="home_social-icon" data-aos="fade-down"
            ><i class="bx bxl-facebook-circle"></i
          ></a>
          <a
            href="#"
            class="home_social-icon"
            data-aos="fade-down"
            data-aos-delay="250"
            ><i class="bx bxl-instagram"></i
          ></a>
          <a
            href="#"
            class="home_social-icon"
            data-aos="fade-down"
            data-aos-delay="300"
            ><i class="bx bxl-twitter"></i
          ></a>
          <a
            href="#"
            class="home_social-icon"
            data-aos="fade-down"
            data-aos-delay="350"
            ><i class="bx bxl-github"></i
          ></a>
        </div>

        <div class="home_img" data-aos="fade-down" data-aos-delay="500">
          <svg
            id="a154b3ae-224e-4b43-86b8-0ffeb27982c5"
            data-name="Layer 1"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 1144 637"
          >
            <title>working remotely</title>
            <path
              d="M1172,547.81a180.56,180.56,0,0,1-26.12,93.88c0,34.62-16.14,66-42.32,88.87a144.74,144.74,0,0,1-21.08,15.28c-.3.19-.61.37-.92.55-.56.33-1.12.66-1.69,1l-.53.31h0c-2.39,1.35-4.83,2.65-7.32,3.87a165.67,165.67,0,0,1-73.76,17H245.17q-9,0-17.84-.72a211.15,211.15,0,0,1-61.06-14.14q-5.72-2.26-11.22-4.86-2.62-1.23-5.19-2.53c-1.07-.54-2.14-1.1-3.2-1.66A190.5,190.5,0,0,1,128,733.32a183.89,183.89,0,0,1-15.8-12.12C78.17,692,57.12,651.59,57.12,607A180.5,180.5,0,0,1,28,508.32c0-99.14,79.24-179.51,177-179.51,3,0,6,.09,9,.25.43,0,.85,0,1.28.06,16.48-28.09,38.51-53.9,65-76.62,72.24-61.9,177.82-100.92,295.43-100.92,98.82,0,189.15,27.55,258.34,73.07A174.18,174.18,0,0,1,920,202.1c97.74,0,177,80.37,177,179.51a184.9,184.9,0,0,1-1,18.78A180,180,0,0,1,1172,547.81Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
              opacity="0.1"
            />
            <path
              d="M938.69,405.47V394.74a39.05,39.05,0,1,0-29.38,0v10.73A55,55,0,0,0,883.77,421a55.08,55.08,0,0,0-31.08-22.52V387.74a39.05,39.05,0,1,0-29.38,0v10.73a55,55,0,0,0-23.21,13.16,55.08,55.08,0,0,0-29.41-20.16V380.74a39.05,39.05,0,1,0-29.38,0v10.73a55,55,0,0,0-26,16.06,55.09,55.09,0,0,0-36.57-33.06V363.74a39.05,39.05,0,1,0-29.38,0v10.73a55,55,0,0,0-40,47.77,54.62,54.62,0,0,0-16.57-7.77V403.74a39.05,39.05,0,1,0-29.38,0v10.73a55.18,55.18,0,0,0-34.66,28.7,54.58,54.58,0,0,0-15-6.7V425.74a39.05,39.05,0,1,0-29.38,0v10.73a54.29,54.29,0,0,0-14.21,6.22,55.14,55.14,0,0,0-34.41-28.22V403.74a39.05,39.05,0,1,0-29.38,0v10.73a55.1,55.1,0,0,0-35.87,31.36,55,55,0,0,0-18.75-9.36V425.74a39.05,39.05,0,1,0-29.38,0v10.73a55,55,0,0,0-40.31,53v248H392v-22h52v22H554v-22h79v-40h68v17h82v7h86v7H979v-248A55,55,0,0,0,938.69,405.47Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
              opacity="0.1"
            />
            <path
              d="M490.78,169h91.43A170.28,170.28,0,0,1,752.5,339.28V570a0,0,0,0,1,0,0h-432a0,0,0,0,1,0,0V339.28A170.28,170.28,0,0,1,490.78,169Z"
              fill="#2f2e41"
            />
            <path
              d="M500.78,178.28h71.43A170.28,170.28,0,0,1,742.5,348.56V560.71a0,0,0,0,1,0,0h-412a0,0,0,0,1,0,0V348.56A170.28,170.28,0,0,1,500.78,178.28Z"
              opacity="0.2"
            />
            <path
              d="M1072,734.09v17.46a165.67,165.67,0,0,1-73.76,17H245.17q-9,0-17.84-.72a211.15,211.15,0,0,1-61.06-14.14q-5.72-2.26-11.22-4.86-2.62-1.23-5.19-2.53c-1.07-.54-2.14-1.1-3.2-1.66A190.5,190.5,0,0,1,128,733.32V685.9A28.9,28.9,0,0,1,156.9,657H988.13a28.9,28.9,0,0,1,19,7.17l55,48.2A28.87,28.87,0,0,1,1072,734.09Z"
              transform="translate(-28 -131.5)"
              fill="#2f2e41"
            />
            <path
              d="M510.67,357.31q-32.71,2.16-65.17,7c-6.15.92-12.39,1.94-18,4.66a52.8,52.8,0,0,0-11.94,8.56,157.38,157.38,0,0,0-38,51.53c-5.57,12.15-9.57,25-14.82,37.25-18.69,43.75-52.59,79.53-72.32,122.82-4.27,9.37-7.87,19.15-9.3,29.34-1.48,10.54.2,22.84,8.86,29,4,2.83,8.86,4,13.62,5a1641.51,1641.51,0,0,0,181.57,29.65c-6.61-6.38-8.82-16.27-7.95-25.41s4.46-17.78,8-26.25q-51.81-11.43-103.36-24c-5.13-1.25-11.29-3.6-11.92-8.84-.32-2.67,1-5.24,2.3-7.59a407.17,407.17,0,0,1,52.4-74c0,28.06-1.39,59.75-1.39,87.82H747.35a248,248,0,0,1-6.84-48.85C739,501.24,757.1,447.89,752.4,394.24c-.44-4.95-1.12-10.05-3.71-14.29-4.47-7.32-13.39-10.35-21.59-12.85-31.44-9.56-63.54-19.23-96.4-18.48-9.77.23-19.5,1.37-29.21,2.52C571.9,354.63,540.4,355.34,510.67,357.31Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <path
              d="M358.88,679.82l23.6,75.53a2.36,2.36,0,0,0,2.25,1.65H486l-24-88-101.06,7.77A2.36,2.36,0,0,0,358.88,679.82Z"
              transform="translate(-28 -131.5)"
              fill="#656478"
            />
            <path
              d="M532,389.79c-4.4,2.53-9.53,3.44-14.53,4.31l-32.27,5.6c-6.28,1.09-12.89,2.33-17.73,6.48-9.9,8.47-7.76,24.06-4.76,36.74l6,25.44c4.52,19.12,9.14,38.47,18.41,55.79,16.19,30.23,45.89,52,78.55,62.49,11.67,3.75,24,6.19,36.18,4.85,23.86-2.62,44.27-19.63,56.85-40.08s18.57-44.17,24.06-67.55c5.27-22.38,10.28-45.08,9.94-68.08-.1-7.16-.82-14.64-4.64-20.71-8.37-13.33-27.34-14.33-42.89-11.87-2.42.39-4.93.81-7.26.08-7-2.18-7.16-11.79-10.16-18.46-5.67-12.58-22.49-14.81-36.24-13.67s-35.16,2.61-47.14,10.4C532.85,369,545.51,382,532,389.79Z"
              transform="translate(-28 -131.5)"
              fill="#fbbebe"
            />
            <path
              d="M532,389.79c-4.4,2.53-9.53,3.44-14.53,4.31l-32.27,5.6c-6.28,1.09-12.89,2.33-17.73,6.48-9.9,8.47-7.76,24.06-4.76,36.74l6,25.44c4.52,19.12,9.14,38.47,18.41,55.79,16.19,30.23,45.89,52,78.55,62.49,11.67,3.75,24,6.19,36.18,4.85,23.86-2.62,44.27-19.63,56.85-40.08s18.57-44.17,24.06-67.55c5.27-22.38,10.28-45.08,9.94-68.08-.1-7.16-.82-14.64-4.64-20.71-8.37-13.33-27.34-14.33-42.89-11.87-2.42.39-4.93.81-7.26.08-7-2.18-7.16-11.79-10.16-18.46-5.67-12.58-22.49-14.81-36.24-13.67s-35.16,2.61-47.14,10.4C532.85,369,545.51,382,532,389.79Z"
              transform="translate(-28 -131.5)"
              opacity="0.1"
            />
            <path
              d="M505.29,418.45c4.88,10.24,8.54,21.1,14.44,30.79,4.69,7.7,10.7,14.49,16.68,21.24C551.9,488,567.59,505.66,586.76,519a222.93,222.93,0,0,1,55.37-109c8.26-8.87,18.6-17.61,30.72-17.28,7.52.21,14.46,3.94,20.72,8.09,7,4.63,13.62,10,18.65,16.67,7.95,10.62,11.38,24.07,12,37.32s-1.44,26.47-3.48,39.57l-10.5,67.71c-.61,3.92-1.46,8.25-4.66,10.6a14.67,14.67,0,0,1-6,2.16c-38.17,7.43-77.51,2.61-116.4,2.23-43-.41-87.19,4.49-127.92-9.19-2.13-.72-4.34-1.55-5.78-3.26a12.06,12.06,0,0,1-2-4.31c-9.49-30.72-1.88-63.73,3.75-95.38a748.38,748.38,0,0,0,9.51-75.78c.17-2.29,25.33,2.77,28.14,4.39C496.53,398.07,501.61,410.73,505.29,418.45Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <g opacity="0.2">
              <path
                d="M194.87,668.29c0,.46-.05.91-.1,1.35q-5.72-2.26-11.22-4.86a9.1,9.1,0,0,1-5.19-2.53c-1.07-.54-2.14-1.1-3.2-1.66a13.68,13.68,0,0,1,.81-1.46c2.06-3.26,5.19-5.3,8.64-5.19s6.44,2.34,8.29,5.71A16.87,16.87,0,0,1,194.87,668.29Z"
                transform="translate(-28 -131.5)"
                fill="#3f3d56"
              />
              <path
                d="M195.41,651.17a16.88,16.88,0,0,1-2.51,8.48c-2.06,3.25-5.19,5.29-8.64,5.18l-.71-.05a9.1,9.1,0,0,1-5.19-2.53,12.53,12.53,0,0,1-2.39-3.12,17.55,17.55,0,0,1,.54-17.12c2.06-3.26,5.19-5.3,8.64-5.19s6.44,2.34,8.29,5.71A16.87,16.87,0,0,1,195.41,651.17Z"
                transform="translate(-28 -131.5)"
                fill="#3f3d56"
              />
              <ellipse
                cx="185.25"
                cy="633.7"
                rx="14.01"
                ry="10.7"
                transform="translate(-481.98 667.38) rotate(-88.19)"
                fill="#3f3d56"
              />
              <ellipse
                cx="185.79"
                cy="616.59"
                rx="14.01"
                ry="10.7"
                transform="translate(-464.35 651.34) rotate(-88.19)"
                fill="#3f3d56"
              />
              <ellipse
                cx="186.33"
                cy="599.47"
                rx="14.01"
                ry="10.7"
                transform="translate(-446.72 635.3) rotate(-88.19)"
                fill="#3f3d56"
              />
              <path
                d="M150,481.05a49.66,49.66,0,0,1-3.8-6l28.26-3.73L144,470.6a51.38,51.38,0,0,1,.31-40.64l40.12,22.44-36.75-28.84a51.28,51.28,0,1,1,82.84,60,51.12,51.12,0,0,1,5.55,9.53L199,510.93l39.33-11.83A51.34,51.34,0,0,1,228.53,547,51.28,51.28,0,1,1,148,544.43a51.28,51.28,0,0,1,2-63.38Z"
                transform="translate(-28 -131.5)"
                fill="#6c63ff"
              />
              <path
                d="M240.5,515.62a51.06,51.06,0,0,1-12,31.35A51.28,51.28,0,1,1,148,544.43C141.37,535.49,240.68,509.87,240.5,515.62Z"
                transform="translate(-28 -131.5)"
                opacity="0.1"
              />
            </g>
            <circle
              cx="68.02"
              cy="141.18"
              r="21.63"
              fill="#6c63ff"
              opacity="0.1"
            />
            <circle
              cx="158.17"
              cy="21.63"
              r="21.63"
              fill="#6c63ff"
              opacity="0.1"
            />
            <circle
              cx="150.84"
              cy="103.76"
              r="36.25"
              fill="#6c63ff"
              opacity="0.1"
            />
            <circle cx="543" cy="185.5" r="84" fill="#fbbebe" />
            <path
              d="M536.88,152.17c-22.41,2.84-46.6,6.59-62.44,22.69-8.86,9-14.05,21-18.32,32.88-6.62,18.5-11.55,38-10,57.63,1.38,17.56,7.88,35.52,2.62,52.34-2.42,7.74-7.17,14.5-10.86,21.71-6.84,13.39-10.06,28.4-11.24,43.39-.82,10.31-.66,20.92,2.73,30.69,3.61,10.4,10.65,19.25,15.11,29.31,6.6,14.86,7.26,31.58,7.77,47.83s.94,32.39,1.32,48.58c.24,10.18.26,21.08-5.37,29.57,20.79-8.33,41.87-16.83,59.66-30.43s32.19-33.21,34.49-55.49c1.86-18.06-4.24-35.86-9.5-53.24-13-43-21.4-88.84-11.94-132.75,3.41-15.81,11.7-33.46,27.61-36.37,9.71-1.77,19.4,2.66,28.15,7.24,20.68,10.82,42,24.82,49.7,46.85,7,19.92,1.11,42.11-8,61.13s-21.51,36.51-28.59,56.39c-10.87,30.5-7.81,66.21,10.25,93.08s51.43,43.4,83.52,39.06c-2.51-10.84-10.38-19.6-14.6-29.9-7.67-18.71-2.5-40.23,5.75-58.69S694.21,440,699.37,420.4c3.64-13.8,4.08-28.22,4.06-42.49,0-22.46-1.11-44.93-3.27-67.29s-5.46-45-12.58-66.51c-5.72-17.25-14.05-33.93-26.51-47.16-13.26-14.09-30.52-23.64-47.47-33-10.14-5.58-20.5-11.23-31.88-13.32-9-1.65-18.46-4-27.64-4.15C547.84,146.39,541.28,147.74,536.88,152.17Z"
              transform="translate(-28 -131.5)"
              fill="#434175"
            />
            <rect
              x="624.01"
              y="254.09"
              width="60.85"
              height="141.74"
              rx="2.9"
              transform="translate(45.9 -250.24) rotate(10.98)"
              fill="#656478"
            />
            <rect
              x="628.09"
              y="254.88"
              width="60.85"
              height="141.74"
              rx="2.9"
              transform="translate(46.13 -251) rotate(10.98)"
              fill="#3f3d56"
            />
            <ellipse
              cx="666.17"
              cy="286.29"
              rx="10.05"
              ry="4.15"
              transform="translate(230.2 754.21) rotate(-79.02)"
              fill="#6c63ff"
            />
            <path
              d="M683,332.5c-2.64-4.67-5.46-9.5-9.91-12.49a35,35,0,0,0-8.18-3.67c-9.69-3.39-19.54-6.81-29.79-7.35-1.67-.08-3.58,0-4.67,1.28-2.24,2.63,1.31,6.21,4.38,7.8l24.42,12.65-22.51-2.38c-3.27-.35-7.93.54-7.69,3.82.16,2.15,2.52,3.32,4.56,4,14.45,5,31.15,8.92,39.06,22-10.54-1-21.31-2-31.64.32-2.83.64-5.76,1.63-7.61,3.86s-2.06,6,.27,7.77c1.44,1.07,3.38,1.1,5.18,1,7.33-.35,14.85-1.81,21.89.28s13.29,9.47,10.86,16.39c6.24.56,13.62,0,19.39-2.69,6.36-3,6.21-8.64,5.82-15.44C696,356.33,689.39,343.9,683,332.5Z"
              transform="translate(-28 -131.5)"
              fill="#fbbebe"
            />
            <path
              d="M676.69,550.49a1125.21,1125.21,0,0,0-23-116.92c-5-20-10.68-40.34-9.25-60.92,20.66,2.63,39.17,4.58,58.21-3.86.31,10.81,8.15,20,11,30.45,1.91,7,1.19,14.41,1.94,21.62s3,14.2,4.93,21.21a260.23,260.23,0,0,1,6.63,106.74C709.48,550.91,694.32,553.22,676.69,550.49Z"
              transform="translate(-28 -131.5)"
              opacity="0.1"
            />
            <path
              d="M673.69,550.49a1125.21,1125.21,0,0,0-23-116.92c-5-20-10.68-40.34-9.25-60.92,20.66,2.63,39.17,4.58,58.21-3.86.31,10.81,8.15,20,11,30.45,1.91,7,1.19,14.41,1.94,21.62s3,14.2,4.93,21.21a260.23,260.23,0,0,1,6.63,106.74C706.48,550.91,691.32,553.22,673.69,550.49Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <path
              d="M384.63,745.27l9.79-242.87a14.86,14.86,0,0,1,15-14.26l386.52,3.7A14.86,14.86,0,0,1,810.59,508L790.17,740.67a14.86,14.86,0,0,1-14.55,13.56l-375.88,6.5A14.87,14.87,0,0,1,384.63,745.27Z"
              transform="translate(-28 -131.5)"
              fill="#3f3d56"
            />
            <ellipse cx="572.5" cy="467" rx="17" ry="20" fill="#6c63ff" />
            <path
              d="M964,584.76l-.8,6.86-13,110.86c-33.89,23.63-60.25.92-60.48,0L873.34,591.1l-.93-6.34Z"
              transform="translate(-28 -131.5)"
              fill="#3f3d56"
            />
            <path
              d="M964,584.76l-.8,6.86c-38.18,22.2-78.91,4.92-89.86-.52l-.93-6.34Z"
              transform="translate(-28 -131.5)"
              opacity="0.1"
            />
            <path
              d="M870.5,578.74v10s50.5,29.36,96,0v-10Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <path
              d="M876.37,565.53s-1.47,6.75-5.87,7.34v8.51h96v-7.63s-5.87-1.47-5-8.22Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <ellipse
              cx="890.21"
              cy="434.76"
              rx="43.3"
              ry="12.48"
              fill="#6c63ff"
            />
            <ellipse
              cx="890.21"
              cy="434.76"
              rx="43.3"
              ry="12.48"
              opacity="0.1"
            />
            <path
              d="M956.22,565.53c0,5-16.42,9.1-36.69,9.1h-1.08c-13.61-.1-25.37-2-31.37-4.84-2.71-1.28-4.25-2.73-4.25-4.26,0-2.54,4.2-4.84,11-6.49a113.49,113.49,0,0,1,25.73-2.61C939.8,556.43,956.22,560.5,956.22,565.53Z"
              transform="translate(-28 -131.5)"
              opacity="0.1"
            />
            <path
              d="M918.45,574.63c-13.61-.1-25.37-2-31.37-4.84h0L893.8,559Z"
              transform="translate(-28 -131.5)"
              opacity="0.1"
            />
            <path
              d="M880.1,566.23c-.52-.11-1.21.07-1.31.59a1.27,1.27,0,0,0,.2.75,10.67,10.67,0,0,0,4.78,4.09,2.85,2.85,0,0,0,1.09.35,1,1,0,0,0,1-.52,1.13,1.13,0,0,0-.07-.93,4.13,4.13,0,0,0-1.24-1.36C883.21,568.15,881.84,566.52,880.1,566.23Z"
              transform="translate(-28 -131.5)"
              opacity="0.1"
            />
            <circle cx="891.67" cy="515.79" r="25.83" fill="#6c63ff" />
            <path
              d="M188.33,515.85h12.11a25,25,0,0,1,25,25V578a0,0,0,0,1,0,0H163.33a0,0,0,0,1,0,0V540.85A25,25,0,0,1,188.33,515.85Z"
              fill="#3f3d56"
            />
            <path
              d="M188.33,515.85h12.11a25,25,0,0,1,25,25V578a0,0,0,0,1,0,0H163.33a0,0,0,0,1,0,0V540.85A25,25,0,0,1,188.33,515.85Z"
              opacity="0.1"
            />
            <circle cx="191.9" cy="524.55" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="518.34" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="512.12" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="505.91" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="499.7" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="493.49" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="487.28" r="4.97" fill="#3f3d56" />
            <circle cx="199.36" cy="489.76" r="4.97" fill="#3f3d56" />
            <circle cx="204.33" cy="487.28" r="4.97" fill="#3f3d56" />
            <circle cx="209.3" cy="484.79" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="481.07" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="474.86" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="468.64" r="4.97" fill="#3f3d56" />
            <circle cx="191.9" cy="462.43" r="4.97" fill="#3f3d56" />
            <path
              d="M240.5,577.91c-1.23.18-2.47.31-3.71.39A28.56,28.56,0,0,0,240,575a21.22,21.22,0,0,0-3-5.83,10.22,10.22,0,0,1-4,1.26c-1.23.18-2.47.31-3.71.4,1.63-1.33,3.15-3.33,4.75-5a21.09,21.09,0,1,0,6.61,12Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <path
              d="M257.11,602.6a9.68,9.68,0,0,1-4.18,1.39c-1.23.18-2.47.32-3.71.4a36.4,36.4,0,0,0,3.68-3.82,12.44,12.44,0,1,0,4.21,2Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <circle cx="184.45" cy="489.76" r="4.97" fill="#3f3d56" />
            <circle cx="179.48" cy="487.28" r="4.97" fill="#3f3d56" />
            <circle cx="174.51" cy="484.79" r="4.97" fill="#3f3d56" />
            <path
              d="M182.7,602.6a9.64,9.64,0,0,0,4.18,1.39c1.23.18,2.47.32,3.71.4a35.42,35.42,0,0,1-3.68-3.82,12.44,12.44,0,1,1-4.21,2Z"
              transform="translate(-28 -131.5)"
              fill="#6c63ff"
            />
            <path
              d="M188.33,519.58h12.11a25,25,0,0,1,25,25v32.87a4.24,4.24,0,0,1-4.24,4.24H167.57a4.24,4.24,0,0,1-4.24-4.24V544.58a25,25,0,0,1,25-25Z"
              fill="#3f3d56"
            />
            <g opacity="0.1">
              <path
                d="M240.88,579.27a18.83,18.83,0,0,1-1.6,1.52c.57,0,1.13-.09,1.7-.15C241,580.18,240.93,579.72,240.88,579.27Z"
                transform="translate(-28 -131.5)"
              />
              <path
                d="M231.82,573.33c1.25-.08,2.48-.21,3.72-.39a12,12,0,0,0,3.23-.88,21.28,21.28,0,0,0-1.74-2.87,7.52,7.52,0,0,1-2,.85A28.79,28.79,0,0,1,231.82,573.33Z"
                transform="translate(-28 -131.5)"
              />
              <path
                d="M201.27,584a21.08,21.08,0,0,1,32.5-17.76l.32-.34a21.1,21.1,0,1,0-27.82,31.73A21,21,0,0,1,201.27,584Z"
                transform="translate(-28 -131.5)"
              />
            </g>
            <g opacity="0.1">
              <path
                d="M249.22,606.87c1.24-.08,2.48-.21,3.71-.39a9.7,9.7,0,0,0,4.18-1.4,12.43,12.43,0,0,1,5,8.8,11.38,11.38,0,0,0,.07-1.31,12.38,12.38,0,0,0-5-10,9.68,9.68,0,0,1-4.18,1.39l-1,.13A25.37,25.37,0,0,1,249.22,606.87Z"
                transform="translate(-28 -131.5)"
              />
              <path
                d="M249.72,602.63a10.19,10.19,0,0,1,1.24.09c.65-.69,1.29-1.43,1.94-2.15a12.4,12.4,0,0,0-15.6,12c0,.42,0,.83.06,1.24A12.42,12.42,0,0,1,249.72,602.63Z"
                transform="translate(-28 -131.5)"
              />
            </g>
            <g opacity="0.1">
              <path
                d="M190.59,606.87c-1.24-.08-2.48-.21-3.71-.39a9.65,9.65,0,0,1-4.18-1.4,12.43,12.43,0,0,0-5,8.8,11.38,11.38,0,0,1-.07-1.31,12.38,12.38,0,0,1,5-10,9.64,9.64,0,0,0,4.18,1.39l1,.13A23.67,23.67,0,0,0,190.59,606.87Z"
                transform="translate(-28 -131.5)"
              />
              <path
                d="M190.09,602.63a10.36,10.36,0,0,0-1.25.09c-.64-.69-1.28-1.43-1.93-2.15a12.4,12.4,0,0,1,15.6,12c0,.42,0,.83-.06,1.24A12.42,12.42,0,0,0,190.09,602.63Z"
                transform="translate(-28 -131.5)"
              />
            </g>
          </svg>
        </div>
      </section>

      <!-- ABOUT SECTION -->
      <section class="about section" id="about">
        <h2 class="section-title" data-aos="fade-down">About</h2>

        <div class="about_container bd_grid">
          <div class="about_img" data-aos="fade-down" data-aos-delay="50">
            <svg
              id="fe80fb2b-bcaf-407e-919b-306adc32f78b"
              data-name="Layer 1"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 1032 741.75278"
            >
              <title>profile</title>
              <line
                y1="741.25278"
                x2="166"
                y2="741.25278"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <rect
                x="243"
                y="127.75278"
                width="737"
                height="499"
                rx="19.39764"
                fill="#f2f2f2"
              />
              <rect
                x="220.5"
                y="96.25278"
                width="737"
                height="499"
                rx="19.39764"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <line
                x1="220.5"
                y1="144.09298"
                x2="957.5"
                y2="144.09298"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <rect
                x="661"
                y="256.25278"
                width="201"
                height="31"
                rx="7.09252"
                fill="#6c63ff"
                opacity="0.3"
              />
              <rect
                x="622.5"
                y="342.25278"
                width="278"
                height="25"
                rx="7.09252"
                fill="#6c63ff"
                opacity="0.3"
              />
              <rect
                x="622.5"
                y="410.25278"
                width="278"
                height="25"
                rx="7.09252"
                fill="#6c63ff"
                opacity="0.3"
              />
              <rect
                x="622.5"
                y="478.25278"
                width="278"
                height="25"
                rx="7.09252"
                fill="#6c63ff"
                opacity="0.3"
              />
              <rect
                x="671"
                y="246.25278"
                width="201"
                height="31"
                rx="7.09252"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <rect
                x="632.5"
                y="332.25278"
                width="278"
                height="25"
                rx="7.09252"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <rect
                x="632.5"
                y="400.25278"
                width="278"
                height="25"
                rx="7.09252"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <rect
                x="632.5"
                y="468.25278"
                width="278"
                height="25"
                rx="7.09252"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <circle
                cx="276.5"
                cy="126.25278"
                r="15"
                fill="#6c63ff"
                opacity="0.3"
              />
              <circle
                cx="318.5"
                cy="126.25278"
                r="15"
                fill="#6c63ff"
                opacity="0.3"
              />
              <circle
                cx="360.5"
                cy="126.25278"
                r="15"
                fill="#6c63ff"
                opacity="0.3"
              />
              <circle
                cx="282.5"
                cy="120.25278"
                r="15"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <circle
                cx="324.5"
                cy="120.25278"
                r="15"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <circle
                cx="366.5"
                cy="120.25278"
                r="15"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <path
                d="M537.854,653.37916c-2.51135-11.56848-3.17724-27.36932-2.33252-38.36047,0,0-12.69836-55.78644-22.68994-60.99133l-.00305.003c-.153.19678-5.00195,6.55383-5.61706,26.22443-.62452,19.98284-7.69971,33.09655-7.69971,33.09655s2.28955,24.90766.98047,40.02777Z"
                transform="translate(-84.5 -79.12639)"
                fill="#6c63ff"
              />
              <path
                d="M630.22827,298.37916H399.77173A23.77169,23.77169,0,0,0,376,322.15083V629.6075a23.77168,23.77168,0,0,0,23.77173,23.77166h80.855c-2.7002-11.19934-6.057-28.69067-2.65735-40.85241l-.00159-.008.0022.00525c.15869-.56757.32727-1.12738.51611-1.67047a63.49747,63.49747,0,0,0,2.29175-24.35407,50.6095,50.6095,0,0,0,0-21.23175c-2.4978-11.65564-4.24634-23.10522-4.24634-23.10522s-1.377-15.40234-.1748-24.84424c.02661-.2074.05762-.404.08667-.60541-.42432-.09655-.66235-.15228-.66235-.15228s3.53881-16.02789,4.78759-26.22748c.29493-2.40783.683-5.46032,1.10315-8.71478a20.93993,20.93993,0,0,1-3.3927-.86035c-11.24035-3.9549-14.779-39.75751-14.779-39.75751V429.656s-3.74683-17.38092,9.36694-25.08258c12.62793-7.41644,17.66968-9.44617,18.02613-9.58643.09619-.06878.19018-.13128.28833-.20727a11.06127,11.06127,0,0,0,3.28967-4.23371q.02619-.42873.01233-.85211c-.21326-4.06665-3.04419-7.76507-5.73047-10.99225q-3.43653-4.12857-6.87341-8.25726a8.07194,8.07194,0,0,1-1.77027-2.86487,6.604,6.604,0,0,1-.187-1.80389q-.00275-.33691.004-.673.056-3.07836.16724-6.15545c.06445-1.79224.51562-4.05353,2.27075-4.42182.91284-.19159,2.12109.14246,2.60364-.65576a1.56534,1.56534,0,0,0,.11682-1.06054c-.00586.02661-.00733.05444-.015.0805-.00586-.03339-.01159-.06695-.01782-.09985a22.43656,22.43656,0,0,1-.65051-4.38636,5.84207,5.84207,0,0,1,.282-1.96984c1.01672-2.97516,4.51782-4.196,7.61133-4.75727,3.09375-.56134,6.56653-1.04425,8.5083-3.51709a26.9506,26.9506,0,0,1,1.68884-2.37384,6.62979,6.62979,0,0,1,3.16589-1.59674,17.49792,17.49792,0,0,1,11.50623,1.02118c1.49646.68286,2.99963,1.60248,4.64124,1.49841,1.70507-.108,3.16162-1.3081,4.84509-1.60009,2.71911-.47156,5.31872,1.56567,6.65869,3.97827a9.85108,9.85108,0,0,1,1.23279,5.02313,6.912,6.912,0,0,1-1.76416,4.74109c-1.17017,1.24145-2.91626,2.09418-3.4021,3.72955-.198.66565-.152,1.38257-.32691,2.05457-.02185.084-.05737.16241-.08606.24365.03211.04169.06714.08112.09888.123a21.231,21.231,0,0,1-10.33215,33.01928c-.00794.21058-.01624.42133-.01514.63306a9.173,9.173,0,0,0,2.8396,7.0647l18.54724,7.606s11.16565-1.3534,15.19495,15.30957a28.82628,28.82628,0,0,1,.68982,8.45746c-.14636,2.51251.19507,6.93573,3.05725,12.66,4.57934,9.15881,3.53857,30.18237-5.82837,32.26392-8.87231,1.97161-12.32361,1.14331-12.66382,1.05023l-.02014.3681c.14612,3.94489,1.55029,37.969,6.64758,42.086,1.40955,1.13849,1.14026,1.90753-.01635,2.42578l.0028.00336s.0094.21856.03113.612c.15308,2.48846.93994,11.96472,4.35254,17.357,3.956,6.24457,3.54077,42.25739,3.54077,42.25739l2.70386,21.23181s-1.66419,13.11371,0,15.4024c.94556,1.29785,2.09057,21.40351,2.905,38.56964h69.53027A23.77168,23.77168,0,0,0,654,629.6075V322.15083A23.77169,23.77169,0,0,0,630.22827,298.37916Z"
                transform="translate(-84.5 -79.12639)"
                fill="#6c63ff"
              />
              <rect
                x="267.5"
                y="192.25278"
                width="278"
                height="355"
                rx="23.77165"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <path
                d="M185.32419,400.757S176,398,174,401s2.72669,24.7477,2.72669,24.7477l20.54589,1.24859-7.17022-18.10653Z"
                transform="translate(-84.5 -79.12639)"
                fill="#2f2e41"
              />
              <path
                d="M113.44417,579.34709s18.69466,41.04232,4.29762,39.753-19.98395-39.753-19.98395-39.753Z"
                transform="translate(-84.5 -79.12639)"
                fill="#a0616a"
              />
              <path
                d="M235.71128,575.07127s-8.20129,44.34751,5.45523,39.61078,9.76437-43.40874,9.76437-43.40874Z"
                transform="translate(-84.5 -79.12639)"
                fill="#a0616a"
              />
              <path
                d="M181.34664,390.46647s-.21488,20.6286,7.73573,21.703-4.51251,12.03335-4.51251,12.03335l-14.18216,2.79346L149.974,425.49212l-9.025-11.60359s15.90121-7.52084,9.025-30.9429Z"
                transform="translate(-84.5 -79.12639)"
                fill="#a0616a"
              />
              <path
                d="M181.34664,390.46647s-.21488,20.6286,7.73573,21.703-4.51251,12.03335-4.51251,12.03335l-14.18216,2.79346L149.974,425.49212l-9.025-11.60359s15.90121-7.52084,9.025-30.9429Z"
                transform="translate(-84.5 -79.12639)"
                opacity="0.1"
              />
              <path
                d="M217.87645,564.95005s10.09942,21.703,2.14881,89.82036c0,0,2.3637,24.0667.42977,28.5792s-17.83515,65.75367-17.83515,65.75367-20.41371,4.5125-23.20717-9.025c0,0,2.79346-19.33931,2.57857-22.34765s4.51251-35.88516,4.51251-35.88516l-9.66966-63.60485-7.306,57.37329s0,16.54586-2.36369,20.19884,0,77.14236,0,77.14236,6.66132,11.17383-3.4381,11.38871-19.12443-.21488-19.984-7.306-1.28929-14.18216-3.4381-18.47979-4.94227-53.50543-4.29762-70.69593-14.18216-105.50669-9.45478-114.74659S217.87645,564.95005,217.87645,564.95005Z"
                transform="translate(-84.5 -79.12639)"
                fill="#2f2e41"
              />
              <circle cx="85.8877" cy="293.29006" r="25.78575" fill="#a0616a" />
              <path
                d="M144.60195,414.31829s15.68633,11.60359,38.46374,2.3637c0,0,7.52084-3.653,6.8762-9.2399s15.68633,44.91018,15.68633,44.91018l16.54586,87.88643-.85953,35.88517s-7.306-3.653-30.08337,4.51251-59.95187-9.2399-59.95187-9.2399l1.28929-92.18405,1.28928-53.72031,3.4381-11.81847S139.015,410.45043,144.60195,414.31829Z"
                transform="translate(-84.5 -79.12639)"
                fill="#f2f2f2"
              />
              <path
                d="M182.06324,399.89323s3.79591-.61662,7.44889,5.18517,12.24823,9.45477,12.24823,9.45477,20.84348,1.28929,23.85182,12.46312,10.52918,26.43039,14.18216,54.57983,10.95894,73.05963,12.03335,76.71261-1.50417,14.8268,1.50417,18.2649-21.27325,3.4381-21.27325,3.4381-2.14881-17.62026-3.653-17.62026-1.0744,11.81847.42977,20.41372-10.95895,0-10.95895,0-9.66965-39.32327-18.90955-74.77867S184.355,452.99692,186.074,445.04631s6.44644-30.728,3.00834-32.87683S182.06324,399.89323,182.06324,399.89323Z"
                transform="translate(-84.5 -79.12639)"
                fill="#2f2e41"
              />
              <path
                d="M151.07551,399.87428s-5.614,3.05531-19.7962,13.15473-23.85182,17.83514-23.85182,17.83514-5.58691,4.29762-9.025,29.86849S87.22865,552.48693,90.237,560.8673s4.08275,13.32264,3.00834,18.26491,22.56253,4.72739,22.99229,3.653-.64464-20.6286.42977-21.05836,6.87619,11.60359,7.9506,21.703,13.53752,18.05,16.331,18.05,17.1905-58.23282,17.40538-97.98585-4.72739-73.2745-8.38037-78.00189S151.07551,399.87428,151.07551,399.87428Z"
                transform="translate(-84.5 -79.12639)"
                fill="#2f2e41"
              />
              <path
                d="M188.86748,751.03721s1.71905-4.72739,7.73573-3.22322,10.09942-3.86786,10.09942-3.86786,3.22322-.42977,1.0744,3.653-3.86786,6.8762-3.86786,6.8762,12.89288,29.43873,4.51251,36.52981-18.05,2.79346-18.05,2.79346-9.45477-6.66132-9.025-24.28159c0,0-.42976-5.58691-5.58691-14.61192s-9.025-22.77741-2.79346-25.356,7.83546-2.67436,7.83546-2.67436-2.916,13.33721,4.61624,17.99776Z"
                transform="translate(-84.5 -79.12639)"
                fill="#3f3d56"
              />
              <path
                d="M148.89957,784.3438s-5.15715-9.66966,3.4381-10.74406,17.83515-1.71905,17.40538,2.79345-1.50417,11.38871-1.50417,11.38871l1.50417,4.94227s.42977,12.24823,1.93393,13.7524,9.66966,14.397-7.73572,14.397-22.56253-1.93393-21.05836-6.01667,1.93393-24.28158,1.93393-24.28158Z"
                transform="translate(-84.5 -79.12639)"
                fill="#3f3d56"
              />
              <path
                d="M162.22221,351.78785s12.03335,3.22322,18.26491,4.51251,5.58691-2.3637,5.58691-2.3637,8.16549,1.07441,7.73572.21488,3.4381-5.372-1.0744-10.52918-3.22322-9.025-3.22322-9.025h-3.86786l-1.07441-1.50417h-6.01668s-4.5125-1.71905-16.331,0-27.93456,2.14881-29.22385,9.2399-7.95061,15.90121-5.58691,19.98395,15.90121,20.84348,17.1905,27.93456,7.30933,8.66659,7.09277,4.22585-6.23325-19.91218-1.0761-20.55682S164.5859,360.16822,162.22221,351.78785Z"
                transform="translate(-84.5 -79.12639)"
                fill="#2f2e41"
              />
              <path
                d="M1019.38065,86.58377a22.982,22.982,0,0,0-19.80994,13.851c-4.9535,11.97382,1.42449,26.03885,10.999,34.77028s21.87358,13.72225,33.04831,20.28234c15.00952,8.81128,28.4968,21.04282,36.00691,36.74386s8.30888,35.15009-.51891,50.14991c-8.1937,13.9224-23.09255,22.2549-37.30219,29.9397"
                transform="translate(-84.5 -79.12639)"
                fill="none"
                stroke="#3f3d56"
                stroke-miterlimit="10"
              />
              <ellipse cx="947.5" cy="8.5" rx="17.5" ry="8.5" fill="#6c63ff" />
              <ellipse cx="961.5" cy="64.5" rx="17.5" ry="8.5" fill="#6c63ff" />
              <ellipse cx="929.5" cy="73.5" rx="17.5" ry="8.5" fill="#6c63ff" />
              <ellipse
                cx="979.5"
                cy="120.5"
                rx="17.5"
                ry="8.5"
                fill="#6c63ff"
              />
              <ellipse
                cx="1014.5"
                cy="120.5"
                rx="17.5"
                ry="8.5"
                fill="#6c63ff"
              />
            </svg>
          </div>

          <div>
            <h2
              class="about_subtitle"
              data-aos="fade-down"
              data-aos-delay="350"
            >
              I'm Shiny Sandhya
            </h2>
            <p class="about_text" data-aos="fade-down" data-aos-delay="450">
                "Hi, I'm Shiny Sandhya, currently pursuing a degree in Computer Science and Engineering at Jeppiaar University, Chennai. I am passionate about web development and aspire to create efficient and user-friendly websites. I have experience in HTML, CSS, and JavaScript, and I enjoy exploring new web technologies.

                I possess leadership qualities and have been actively involved in organizing events and leading teams. I am dedicated, detail-oriented, and thrive in collaborative environments. My goal is to become a skilled web developer and contribute innovative solutions to the tech industry.
                
                I am excited about the opportunities ahead and look forward to making a positive impact in web development."
            </p>
          </div>
        </div>
      </section>

      <!-- SKILLS SECTION -->
      <section class="skills section" id="skills">
        <h2 class="section-title" data-aos="fade-down">Skills</h2>

        <div class="skills_container bd_grid">
          <div>
            <h2
              class="skills_subtitle"
              data-aos="fade-down"
              data-aos-delay="250"
            >
              Professional Skills
            </h2>
           
            <!-- SKILLS MICROSOFT -->
            <div class="skills_data" data-aos="fade-right" data-aos-delay="250">
              <div class="skills_name">
                <i class='bx bxl-microsoft' style='color:#4070f4'  ></i>
                <span class="skill_name">Microsoft</span>
              </div>

              <div><span class="skill_percentage">95%</span></div>

              <div class="skill_bar skill_ui"></div>
            </div>
            <!-- SKILLS EDITING -->
            <div class="skills_data" data-aos="fade-right" data-aos-delay="250">
              <div class="skills_name">
                <i class='bx bx-video' style='color:#4070f4' ></i>
                <span class="skill_name">Editing</span>
              </div>

              <div><span class="skill_percentage">95%</span></div>

              <div class="skill_bar skill_ui"></div>
            </div>

             <!-- SKILLS HTML -->
             <div class="skills_data" data-aos="fade-right">
              <div class="skills_name">
                <i class="bx bxl-html5 skill_icon"></i>
                <span class="skill_name">Html5</span>
              </div>

              <div><span class="skill_percentage">75%</span></div>

              <div class="skill_bar skill_html"></div>
            </div>

            <!-- SKILLS css -->
            <div class="skills_data" data-aos="fade-right" data-aos-delay="250">
              <div class="skills_name">
                <i class="bx bxl-css3 skill_icon"></i>
                <span class="skill_name">CSS3</span>
              </div>

              <div><span class="skill_percentage">65%</span></div>

              <div class="skill_bar skill_css"></div>
            </div>
            <!-- SKILLS JS -->
            <div class="skills_data" data-aos="fade-right" data-aos-delay="250">
              <div class="skills_name">
                <i class="bx bxl-javascript skill_icon"></i>
                <span class="skill_name">js</span>
              </div>

              <div><span class="skill_percentage">30%</span></div>

              <div class="skill_bar skill_js"></div>
            </div>
          </div>

          <div data-aos="fade-left" data-aos-delay="350">
            <svg
              id="a379d9a4-f6fe-40d1-beba-a0916853bd02"
              data-name="Layer 1"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 938.75919 806.74836"
            >
              <circle
                cx="75.36532"
                cy="147.52379"
                r="75.36532"
                fill="#ff6584"
              />
              <path
                d="M1004.987,679.01278a136.64937,136.64937,0,0,1-6.38326,37.7743c-.08893.28379-.18213.56334-.2753.84715H974.50666c.02541-.25416.05085-.538.07627-.84715,1.5884-18.26028,10.74606-129.39752-.20334-148.4033C975.33687,569.9256,1006.83381,620.99164,1004.987,679.01278Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#e6e6e6"
              />
              <path
                d="M1003.19956,716.78708c-.19909.28379-.40664.56758-.61842.84715H984.71056c.13555-.24144.29227-.52523.4744-.84715,2.95233-5.32856,11.69063-21.25916,19.80207-37.7743,8.71716-17.74774,16.71423-36.169,16.04074-42.836C1021.23531,637.68045,1027.267,683.51959,1003.19956,716.78708Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#e6e6e6"
              />
              <rect
                x="253.75919"
                y="669.38465"
                width="685"
                height="2.24072"
                fill="#e6e6e6"
              />
              <path
                d="M822.84364,785.9808l3.32758-27.45259,94.00433-24.125-10.81466-32.444c7.53317-21.60748,20.759-32.2,44.92242-21.62931l41.56416,25.82015a26.533,26.533,0,0,1,12.49331,23.97036v0a26.51238,26.51238,0,0,1-15.09493,22.535C946.71544,774.71149,887.41112,783.15126,822.84364,785.9808Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#ffb8b8"
              />
              <path
                d="M828.66691,794.29977l-29.11638-4.15948-27.23329,5.55781a11.76263,11.76263,0,0,1-14.1045-11.0354v0a11.76267,11.76267,0,0,1,4.67429-9.88433l42.67473-32.15219A19.2662,19.2662,0,0,1,830.519,744.136l10.62634,10.23277c-7.60426,4.71745-13.25855,11.79578-16.63793,21.62931Q835.46964,782.0244,828.66691,794.29977Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#2f2e41"
              />
              <circle
                cx="725.85545"
                cy="432.52561"
                r="26.92727"
                fill="#ffb8b8"
              />
              <path
                d="M898.54623,532.25232l-60.31251,25.37284c4.90182-24.6117,7.3447-47.03168,0-60.72845l38.6832-4.57544C874.99682,502.84723,884.78379,516.94354,898.54623,532.25232Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#ffb8b8"
              />
              <path
                d="M796.22294,785.14891l-22.46121-1.6638c-13.76-57.37964-20.805-111.61522-17.73-161.1123a27.99719,27.99719,0,0,1,28.55155-26.31008h0a27.95972,27.95972,0,0,1,18.63912,7.698l29.04629,27.64082a119.53382,119.53382,0,0,1,29.4304,43.81895c8.2263,21.54543,5.27317,33.62388-14.36545,31.57272a48.46037,48.46037,0,0,1-31.55432-16.7762l-21.22016-24.66128Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#ffb8b8"
              />
              <path
                d="M778.829,853.33321h0a19.21665,19.21665,0,0,1-16.93815-25.37662l4.38389-12.8594,3.32759-32.444c5.12583-10.45979,12.38523-8.895,20.79742-.8319,5.348-.52506,6.49594-5.87278,5.82327-13.31035l16.86453,22.70225a13.53384,13.53384,0,0,1,1.45034,13.68454l-16.97287,37.23082A19.21666,19.21666,0,0,1,778.829,853.33321Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#2f2e41"
              />
              <path
                d="M991.30271,703.20708c-30.78017,17.46983-40.42721,17.97672-71.12716,30.36423l-26.6207-14.97414c-31.26416,11.56034-53.19528-4.287-76.95044-27.86854,15.54546-25.89253,8.67013-59.53966,18.30173-59.06466l115.21769,36.1875,4.99138,12.47846Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#2f2e41"
              />
              <path
                d="M954.28331,676.17044c-40.6823,17.60906-84.48565-1.03464-121.87286-42.01078l-24.75581-99.97937a8.344,8.344,0,0,1,6.42773-10.32486l28.72679-5.74536,14.14224,22.46121,28.28449-24.9569,30.03793,9.8201A23.19158,23.19158,0,0,1,930.9073,543.455Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#6c63ff"
              />
              <path
                d="M889.66449,760.92835h0a14.69073,14.69073,0,0,1-5.97562-23.22858l19.01689-22.43017,13.31034,7.48707-6.854,27.943A14.69072,14.69072,0,0,1,889.66449,760.92835Z"
                transform="translate(-130.62041 -46.62582)"
                opacity="0.2"
              />
              <path
                d="M889.66449,757.60077l0,0a14.69073,14.69073,0,0,1-5.97562-23.22858L902.70572,711.942l13.31034,7.48707-6.854,27.943A14.69073,14.69073,0,0,1,889.66449,757.60077Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#ffb8b8"
              />
              <path
                d="M919.34365,726.08424,899.37813,712.7739l29.11638-77.3664L917.67986,526.429l9.86544,6.1659a46.09758,46.09758,0,0,1,20.72563,29.82761l15.99514,77.97633C957.26725,676.34074,945.60181,707.96424,919.34365,726.08424Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#6c63ff"
              />
              <polygon
                points="776.661 555.922 786.644 605.836 778.433 635.028 776.661 555.922"
                opacity="0.2"
              />
              <path
                d="M830.14152,476.84239s-15.517-50.78312,31.90729-40.13255c7.3558,1.652,13.71081,5.92791,18.76625,11.52072a4.56981,4.56981,0,0,0,3.57247,1.45942c7.57575,0,12.25524,27.07165-2.89626,38.97641,0,0,3.0916-16.01961-2.528-21.47812a12.0563,12.0563,0,0,1-2.5013-3.22058c-3.65758-7.37809-15.95243-9.79984-24.432-9.17173-4.329.32067-4.70747,7.8684-9.4997,6.81418C831.62612,459.21134,828.1454,471.843,830.14152,476.84239Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#2f2e41"
              />
              <path
                d="M877.87455,552.21622l-.3135,2.29926-1.93792,14.18773-3.17365,23.23436-.79455,5.81721a1.85307,1.85307,0,0,1-1.83645,1.60276H848.65539a1.85358,1.85358,0,0,1-1.83647-1.59825l-.80823-5.82172-3.22718-23.23436-1.97213-14.19807-.31689-2.2845a1.85321,1.85321,0,0,1,1.83531-2.10888h33.70831a1.85417,1.85417,0,0,1,1.83644,2.10446Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#e6e6e6"
              />
              <path
                d="M713.94258,497.33038H743.294a1.85356,1.85356,0,0,1,1.85356,1.85356v2.44864a1.85351,1.85351,0,0,1-1.85351,1.85351H713.94263a1.85356,1.85356,0,0,1-1.85356-1.85356V499.1839A1.85351,1.85351,0,0,1,713.94258,497.33038Z"
                fill="#3f3d56"
              />
              <path
                d="M880.52618,553.18977a196.18942,196.18942,0,0,1-42.57495,0,1.85342,1.85342,0,0,1-1.85346-1.85341h0v-2.44879a1.85343,1.85343,0,0,1,1.85346-1.85341,174.44189,174.44189,0,0,0,42.57495,0,1.85344,1.85344,0,0,1,1.85341,1.85341v2.44879A1.85344,1.85344,0,0,1,880.52618,553.18977Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <circle cx="727.75919" cy="527.00841" r="8" fill="#fff" />
              <path
                d="M878.94621,590.46462v0A14.69073,14.69073,0,0,1,860.9047,606.269L832.31055,599.404l.68373-15.25628,28.0328-6.47708A14.69073,14.69073,0,0,1,878.94621,590.46462Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#ffb8b8"
              />
              <path
                d="M840.31347,602.13164l-77.1686,1.92921a19.16715,19.16715,0,0,1-19.45354-21.8718v0a19.16712,19.16712,0,0,1,5.88033-11.28657l36.33349-33.9894a48.51883,48.51883,0,0,1,24.20448-12.25587l12.734-2.38762,7.48707,56.569-43.25863-4.99138,50.7457,5.82328Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#6c63ff"
              />
              <path
                d="M738.65069,768.1268H541.64343a6.60576,6.60576,0,0,1-6.60576-6.60576h0q107.12263-12.44971,210.21878,0h0A6.60576,6.60576,0,0,1,738.65069,768.1268Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#2f2e41"
              />
              <path
                d="M745.25645,761.90961,535.03767,761.521l24.36362-40.99461.11657-.19429V629.98469a8.34976,8.34976,0,0,1,8.35046-8.35046H711.26008a8.34976,8.34976,0,0,1,8.35046,8.35046v90.96916Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <path
                d="M567.67792,627.46285a2.72307,2.72307,0,0,0-2.72,2.72v82.37778a2.7232,2.7232,0,0,0,2.72,2.72H712.6162a2.72333,2.72333,0,0,0,2.72-2.72V630.18287a2.7232,2.7232,0,0,0-2.72-2.72Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#fff"
              />
              <path
                d="M568.63047,726.16076a1.169,1.169,0,0,0-1.0591.67849l-7.50719,16.32013a1.16568,1.16568,0,0,0,1.05891,1.653H718.99531a1.1656,1.1656,0,0,0,1.0424-1.68712l-8.16006-16.32012a1.15981,1.15981,0,0,0-1.0424-.64434Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#2f2e41"
              />
              <circle cx="508.94379" cy="577.72843" r="1.74859" fill="#fff" />
              <path
                d="M624.04664,747.92093a1.16751,1.16751,0,0,0-1.1255.86253l-1.8831,6.99434a1.16562,1.16562,0,0,0,1.1255,1.46892H657.976a1.16545,1.16545,0,0,0,1.10121-1.54709l-2.421-6.99434a1.16634,1.16634,0,0,0-1.10159-.78436Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#2f2e41"
              />
              <polygon
                points="588.99 672.346 588.99 673.901 428.781 673.901 428.901 673.706 428.901 672.346 588.99 672.346"
                fill="#2f2e41"
              />
              <path
                d="M491.52194,667.13261a175.14542,175.14542,0,0,0,8.18151,48.41582c.114.36373.23344.722.35286,1.0858H530.589c-.03257-.32576-.06518-.68949-.09775-1.0858-2.03588-23.40445-13.77337-165.85054.26061-190.21049C529.52494,527.3141,489.1549,592.76613,491.52194,667.13261Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#e6e6e6"
              />
              <path
                d="M493.813,715.54843c.25518.36373.5212.72747.79265,1.0858h22.905c-.17373-.30946-.3746-.67319-.608-1.0858-3.784-6.82969-14.984-27.24816-25.38058-48.41582-11.17289-22.74753-21.42285-46.35825-20.55963-54.90349C470.6963,614.15641,462.96541,672.909,493.813,715.54843Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#e6e6e6"
              />
              <path
                d="M545.473,221.78479l12.41349-9.92842c-9.64348-1.06394-13.60582,4.19541-15.22744,8.35823-7.53388-3.12835-15.73541.97151-15.73541.97151l24.83709,9.01675A18.79465,18.79465,0,0,0,545.473,221.78479Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <path
                d="M919.35713,170.6795l12.41349-9.92841c-9.64349-1.06394-13.60582,4.19541-15.22744,8.35823-7.53389-3.12835-15.73541.97151-15.73541.97151l24.83709,9.01674A18.79483,18.79483,0,0,0,919.35713,170.6795Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <path
                d="M847.87608,302.43457l12.41348-9.92842c-9.64348-1.06394-13.60581,4.19541-15.22743,8.35823-7.53389-3.12835-15.73542.97151-15.73542.97151l24.8371,9.01674A18.79481,18.79481,0,0,0,847.87608,302.43457Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <ellipse
                cx="320.01291"
                cy="272.58054"
                rx="112.0821"
                ry="228.69277"
                transform="translate(-173.90826 14.4814) rotate(-10.22048)"
                fill="#e6e6e6"
              />
              <path
                d="M301.65642,229.77517q14.78775,40.21121,26.31876,81.51807,11.509,41.26774,19.68957,83.36863,8.18007,42.08713,12.9707,84.73824,4.767,42.57644,6.1255,85.44331,1.35042,42.82083-.7457,85.65769-.258,5.24814-.56839,10.49347c-.21056,3.58181,5.36184,3.56959,5.57167,0q2.52606-42.97206,1.585-86.05062-.94624-42.83215-5.3194-85.49687-4.38378-42.78927-12.14609-85.146-7.767-42.33823-18.91259-83.9628-11.13864-41.57793-25.61467-82.16468-1.76623-4.94872-3.58171-9.87963c-1.22732-3.33733-6.6142-1.89487-5.37265,1.48117Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <path
                d="M340.048,335.23028l24.68456-54.8093L371.69,264.9728a2.87134,2.87134,0,0,0-.99943-3.81155,2.80754,2.80754,0,0,0-3.81155.99942L342.19442,316.97,335.237,332.41815a2.87134,2.87134,0,0,0,.99943,3.81155,2.80754,2.80754,0,0,0,3.81155-.99942Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <path
                d="M345.50228,372.68041l-56.28535-21.10324-15.86421-5.948a2.80924,2.80924,0,0,0-3.42691,1.94574,2.84665,2.84665,0,0,0,1.94574,3.42691L328.15689,372.105l15.86421,5.948a2.80924,2.80924,0,0,0,3.42691-1.94574,2.84663,2.84663,0,0,0-1.94573-3.42691Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#3f3d56"
              />
              <path
                d="M301.67218,671.62582s67.78868-22.28669,130.93431,0"
                transform="translate(-130.62041 -46.62582)"
                fill="#e6e6e6"
              />
              <path
                d="M604.99788,661.06645c13.43289-.13986,26.86407-.38,40.29636-.5625q6.717-.09126,13.43431-.16c3.85856-.04017,3.86843-6.04028,0-6-13.43289.13986-26.86407.38-40.29636.5625q-6.717.09124-13.43431.16c-3.85856.04017-3.86843,6.04027,0,6Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#6c63ff"
              />
              <path
                d="M604.99788,675.06645l54.29031-.5625,15.44036-.16c3.85858-.04,3.86842-6.04008,0-6l-54.29031.5625-15.44036.16c-3.85858.04-3.86842,6.04008,0,6Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#6c63ff"
              />
              <path
                d="M604.99788,689.06645l54.29031-.5625,15.44036-.16c3.85858-.04,3.86842-6.04008,0-6l-54.29031.5625-15.44036.16c-3.85858.04-3.86842,6.04008,0,6Z"
                transform="translate(-130.62041 -46.62582)"
                fill="#6c63ff"
              />
            </svg>
          </div>
        </div>
      </section>

      <!-- WORK SECTION -->
      <section class="work section" id="work">
        <h2 class="section-title" data-aos="fade-down">Work</h2>

        <div
          class="work_container bd_grid"
          data-aos="fade-down"
          data-aos-delay="250"
        >
          <div class="work_img">
            <img src="https://media.licdn.com/dms/image/D5622AQEUAHWSJZL_MA/feedshare-shrink_2048_1536/0/1716446728392?e=1719446400&v=beta&t=Xtm4umlRcwATMXb8drHBrhhEOVChS4cawRJquhRKCbc" alt="" />
          </div>

          <div class="work_img">
            <img src="https://media.licdn.com/dms/image/D5622AQEFSShezxlYcQ/feedshare-shrink_2048_1536/0/1716446732340?e=1719446400&v=beta&t=fRUM-S2U7oZS_NnmQkyFghUAkDN26r3JfxmWu41R8Uc" alt="" />
          </div>

          <div class="work_img">
            <img src="https://media.licdn.com/dms/image/D5622AQFiPfZf2RPVWA/feedshare-shrink_2048_1536/0/1716446727236?e=1719446400&v=beta&t=xflBBPHnBz-RG1BwxoIjSKNfo9H041pBRFtStFYV_pU" alt="" />
          </div>

          <div class="work_img">
            <img src="https://media.licdn.com/dms/image/D5622AQHJF-jyLjWH1g/feedshare-shrink_2048_1536/0/1716446728848?e=1719446400&v=beta&t=-TsMhE-ctuH2VGS_IKis2M1spN6hL720mrB9e3SNCLY" alt="" />
          </div>

          <div class="work_img">
            <img src="https://media.licdn.com/dms/image/D5622AQElvsBHT3bgug/feedshare-shrink_2048_1536/0/1716446727280?e=1719446400&v=beta&t=IvwLMaoN11Ox4cPzizwtx7ajP_BmR8L7oqQgNECn0d0" alt="" />
          </div>

          <div class="work_img">
            <img src="https://media.licdn.com/dms/image/D5622AQEtYXi6v_AN4Q/feedshare-shrink_2048_1536/0/1716446728354?e=1719446400&v=beta&t=2zV2ESKRaBSYGq-bAfoSErRzQ_TOwfrbB2ynXATj6wg" alt="" />
          </div>
        </div>
      </section>

      <!-- CONTACT SECTION -->

      <section class="contact section" id="contact">
        <h2 class="section-title" data-aos="fade-down">Contact</h2>

        <div class="contact_container bd_grid">
          <form action="#" class="contact_form">
            <input
              type="text"
              placeholder="Name"
              class="control_input"
              data-aos="fade-right"
              data-aos-delay="250"
            />
            <input
              type="mail"
              placeholder="Email"
              class="control_input"
              data-aos="fade-right"
              data-aos-delay="300"
            />
            <textarea
              name=""
              id=""
              cols="0"
              rows="10"
              class="control_input"
              data-aos="fade-right"
              data-aos-delay="400"
            ></textarea>

            <input
              type="button"
              value="Send"
              class="control_button button"
              data-aos="fade-right"
              data-aos-delay="450"
            />
          </form>
        </div>
      </section>

      <!-- Footer Section -->
      <footer class="footer">
        <p class="footer_title" data-aos="fade-down">Shiny Sandhya</p>

        <div class="footer_socials">
          <a
            href="#"
            class="footer_icon"
            data-aos="fade-down"
            data-aos-delay="250"
            ><i class="bx bxl-facebook-circle"></i
          ></a>
          <a
            href="#"
            class="footer_icon"
            data-aos="fade-down"
            data-aos-delay="350"
            ><i class="bx bxl-instagram"></i
          ></a>
          <a
            href="#"
            class="footer_icon"
            data-aos="fade-down"
            data-aos-delay="450"
            ><i class="bx bxl-twitter"></i
          ></a>
          <a
            href="#"
            class="footer_icon"
            data-aos="fade-down"
            data-aos-delay="550"
            ><i class="bx bxl-github"></i
          ></a>
        </div>

        <p data-aos="fade-down" data-aos-delay="650">
          &#169; 2024 copyright all right reserved
        </p>
      </footer>
    </main>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script src="./assets/js/main.js"></script>
    
   
    <script>
      AOS.init({
        duration: 1200,
        once: false,
      });
      // SHOW MENU

const showMenu = (toggleId, navId) => {
    const toggle = document.getElementById(toggleId),
          nav = document.getElementById(navId)

    if(toggle && nav){
          toggle.addEventListener('click', () =>{
                nav.classList.toggle('show')
          });
    }
}

showMenu('nav_toggle','nav_menu')

// ACTIVE & REMOVE ACTIVE
const navLink = document.querySelectorAll('.nav_link')
navLink.forEach(n => n.classList.remove('active'))

function linkAction(){
    navLink.forEach(n => n.classList.remove('active'))
    this.classList.add('active')

    const navMenu = document.getElementById('nav_menu')
    navMenu.classList.remove('show')
}

navLink.forEach(n => n.addEventListener('click', linkAction))
    </script>
  </body>
</html>
