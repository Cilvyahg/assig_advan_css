<!-- 

  & #photo-me {
      border-radius: 50%;
      border: 5px dashed #fff;
      position: absolute;
      inset: 0 50% auto auto;
      transform: translate(50%, -50%);
      width: 12rem;
      height: auto;
      // top: 0;
      // left: 50%;
      // object-position: center;
    }

    
  } -->


  <!-- // OPDRACHT 3: Social Media Buttons

#part-three {
  position: absolute;
  top: 0;
  right: 0;
}

.social_media_laptop {
  background-color: #e17b77;
  display: flex;
  justify-content: space-around;
  align-items: center;
  border: 1px solid black;
  padding: 1rem 1.5rem 1rem 0.5rem;

  img {
    width: 2rem;

    // margin-right: 1rem;
  }
  .social_media_text {
    font-size: 1.3rem;
    font-family: $primary-font;
    padding-left: 0.8rem;
    display: none;
    transition: display 3000ms ease-in;
    
  }
}

.social_media_wrapper:hover .social_media_text {
  display: block;
  
} -->


<!-- // .social_media_wrapper:hover .social_media_text {
//   // transition: opacity 500ms ease-in;
//   // transform: scale(1);
//   // width: 100%;
//   // height: auto;

//   // visibility: visible;
//   // opacity: 1;
// } -->

<!-- last one -->

<!-- // ==================
// Global
// ===================

@import url("https://fonts.googleapis.com/css2?family=Manrope:wght@200&family=Merriweather:wght@300&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Boogaloo&display=swap");
// variables

$primary-font: "Manrope", sans-serif;
$heading-clr: #686de0;
$span-font-big: 2.2rem;
$font-boogaloo: "Boogaloo", cursive;

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}

body {
  background-color: #c3cfe2;
  list-style-type: none;
}

// ========================
// Local
// ========================

// ASSIGNMENT HEADER //
.assignment__header {
  text-align: center;
  margin: 5rem;

  h2 {
    font-family: $font-boogaloo;
    font-size: 3.5rem;
    text-transform: uppercase;
    color: $heading-clr;
  }
}

//OPDRACHT 1 : TESTIMONIAL

#first-part {
  margin-bottom: 10rem;
}

.testimonial {
  width: min(50rem, 80%);
  margin: 0 auto;
  font-family: $primary-font;
  display: flex;
  flex-direction: column;
  justify-content: center;
  border-radius: 20px;
  align-items: center;
  background-color: #fff;
  font-size: 1.4rem;
  overflow: hidden;

  &::before {
    // content: "";
    width: 20px;
    height: 20px;
    background: black;
  }

  // Modififier box shadow

  &.--shadow {
    box-shadow: 0px 7px 20px rgb(70, 70, 70);
  }

  &__header {
    text-align: justify;
    padding: 4rem 3rem 6rem 3rem;
    line-height: 2;

    & span {
      font-size: $span-font-big;
    }
  }

  &__footer {
    margin-top: 2rem;
    width: 100%;
    background-color: $heading-clr;
    position: relative;

    & #photo-me {
      border-radius: 50%;
      border: 5px dashed #fff;
      position: absolute;
      inset: 0 50% auto auto;
      transform: translate(50%, -50%);
      width: 12rem;
    }
  }

  &__text {
    text-align: center;
    padding: 8rem 0 2rem 0;

    h3 {
      text-transform: uppercase;
      color: rgb(229, 173, 207);
      font-family: $font-boogaloo;
      letter-spacing: 0.3em;
      font-size: 1.5em;
    }
    span {
      color: white;
    }
  }
}

// OPDRACHT 2: PORTFOLIO GRID

#second-part {
  margin-bottom: 10rem;
}

.grid__container {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 2em;
  width: min(50%, 300rem);
  margin: 0 auto;

  .grid__item {
    text-align: center;
    position: relative;

    & > img {
      width: 100%;
      height: 100%;
      // object-fit: cover;
      box-shadow: 2px 2px 5px $heading-clr;
      position: relative;
    }
  }
}

.grid__item-cover {
  position: absolute;
  inset: 0 0 0 0;
  background-color: rgb(82, 12, 53);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 500ms ease-out 10ms;

  & > button {
    width: 10rem;
    height: 3rem;
    border-radius: 100px;
    border: none;
    cursor: pointer;

    & a {
      text-decoration: none;
      font-size: 1rem;
      font-family: inherit;
    }
  }
}

// Hover state + border radius

.grid__item:hover {
  border-radius: 10px;
  overflow: hidden;
}

.grid__item-cover:hover {
  opacity: 1;
  border-radius: 10px;
}

//MEDIA QUERIES TABLET/IPAD

@media only screen and (min-width: 768px) {
  .grid__container {
    grid-template-columns: repeat(2, 1fr);
    grid-template-areas:
      "foto1 foto2"
      "foto3 foto4"
      "foto5 foto6"
      "foto7";
  }
}

// MEDIA QUERIES DESKTOP
@media only screen and (min-width: 1200px) {
  .grid__container {
    grid-template-columns: repeat(3, 1fr);
    grid-template-areas:
      "foto1 foto2 foto3"
      "foto4 foto5 foto6"
      "foto7";
  }
}

// OPDRACHT 3: Social Media Buttons

#part-three {
  position: fixed;
  top: 40px;
  right: 0;
  // width: 14rem;

  // display: flex;
  // flex-direction: column;
  // align-items: flex-end;

}

.social_media_wrapper {
 
  
  // float: left;  set position in parent to position absolute// 
  width: 4.5rem;
  margin-left: 9.5rem;
  transition: width 1000ms ease-in, margin-left 1000ms ease-in;
  overflow: hidden;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  height: 3rem;

  &:hover {
    width: 14rem;
    margin-left: 0;
  }
}

.icon-image {
  width: 2rem;
  margin: 0 1rem 0 1.2rem;
}
.social_media_text {
  font-size: 1rem;
  font-family: $primary-font;
  margin-left: 0.5rem;
  white-space: nowrap;
}

//background-color icons

.--laptop {
  background-color: #e17b77;
}

.--twitter {
  background-color: #00aced;
}

.--facebook {
  background-color: #3b5998;
}

.--github {
  background-color: rgb(86, 81, 81);
}
.--linkedin {
  background-color: #007bb6;
}

.--linkedin,
.--facebook,
.--github {
  color: white;
} -->
