<!doctype html>
<html lang="en">

<head>
  <!-- Required meta tags -->
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">

  <title>Hello, world!</title>

  <style type="text/css">
    /* ============ desktop view ============ */
    @media all and (min-width: 992px) {

      .dropdown-menu li {
        position: relative;
      }

      .dropdown-menu .submenu {
        display: none;
        position: absolute;
        left: 100%;
        top: -7px;
      }

      .dropdown-menu .submenu-left {
        right: 100%;
        left: auto;
      }

      .dropdown-menu>li:hover {
        background-color: #f1f1f1
      }

      .dropdown-menu>li:hover>.submenu {
        display: block;
      }
    }

    /* ============ desktop view .end// ============ */

    /* ============ small devices ============ */
    @media (max-width: 991px) {

      .dropdown-menu .dropdown-menu {
        margin-left: 0.7rem;
        margin-right: 0.7rem;
        margin-bottom: .5rem;
      }

    }

    /* ============ small devices .end// ============ */
  </style>
  <script type="text/javascript">
    //	window.addEventListener("resize", function() {
    //		"use strict"; window.location.reload(); 
    //	});


    document.addEventListener("DOMContentLoaded", function () {


      /////// Prevent closing from click inside dropdown
      document.querySelectorAll('.dropdown-menu').forEach(function (element) {
        element.addEventListener('click', function (e) {
          e.stopPropagation();
        });
      })



      // make it as accordion for smaller screens
      if (window.innerWidth < 992) {

        // close all inner dropdowns when parent is closed
        document.querySelectorAll('.navbar .dropdown').forEach(function (everydropdown) {
          everydropdown.addEventListener('hidden.bs.dropdown', function () {
            // after dropdown is hidden, then find all submenus
            this.querySelectorAll('.submenu').forEach(function (everysubmenu) {
              // hide every submenu as well
              everysubmenu.style.display = 'none';
            });
          })
        });

        document.querySelectorAll('.dropdown-menu a').forEach(function (element) {
          element.addEventListener('click', function (e) {

            let nextEl = this.nextElementSibling;
            if (nextEl && nextEl.classList.contains('submenu')) {
              // prevent opening link if link needs to open dropdown
              e.preventDefault();
              console.log(nextEl);
              if (nextEl.style.display == 'block') {
                nextEl.style.display = 'none';
              } else {
                nextEl.style.display = 'block';
              }

            }
          });
        })
      }
      // end if innerWidth

    });
      // DOMContentLoaded  end
  </script>

</head>

<body>
  <h1>ECE Resources</h1>

  <!-- Optional JavaScript; choose one of the two! -->

  <!-- Option 1: Bootstrap Bundle with Popper -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p"
    crossorigin="anonymous"></script>

  <!-- Option 2: Separate Popper and Bootstrap JS -->
  <!--
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>
    -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <a class="navbar-brand" href="https://vce.ac.in/">VCE</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">


          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false"> Year 1 </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#"> SEM 1 » </a>
                <ul class="submenu dropdown-menu">
                  <li><a class="dropdown-item" href="#">ELCS 1</a></li>
                  <li><a class="dropdown-item" href="#">Engineering Mathematics 1</a></li>
                  <li><a class="dropdown-item" href="#">Engineering Chemistry</a></li>
                  <li><a class="dropdown-item" href="#">Programming for Problem Solving</a></li>
                  <li><a class="dropdown-item" href="#">Basic Engineering Mechanics</a></li>
                </ul>
              </li>
              <li><a class="dropdown-item" href="#"> SEM 2 » </a>
                
                <ul class="submenu dropdown-menu">
                  <li><a class="dropdown-item" href="#">ELC 2</a></li>
                  <li><a class="dropdown-item" href="#">Engineering Mathematics 2</a></li>
                  <li><a class="dropdown-item" href="#">Quantum Mechanics and Material Sciences</a></li>
                  <li><a class="dropdown-item" href="#">OOPS</a></li>
                  <li><a class="dropdown-item" href="#">Engineering Drawing</a></li>
                  <li><a class="dropdown-item" href="#">Basics of Electrical Engineering</a></li>
                </ul>
              </li>
            </ul>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false"> Year 2 </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#"> SEM 3 » </a>
                <ul class="submenu dropdown-menu">
                  <li><a class="dropdown-item" href="#">PDENM</a></li>
                  <li><a class="dropdown-item" href="#">Electronic Devices</a></li>
                  <li><a class="dropdown-item" href="#">NATL</a></li>
                  <li><a class="dropdown-item" href="#">EMT</a></li>
                </ul>
              </li>
              <li><a class="dropdown-item" href="#"> SEM 4 » </a>
                
                <ul class="submenu dropdown-menu">
                  <li><a class="dropdown-item" href="#">Electronic Circuits</a></li>
                  <li><a class="dropdown-item" href="#">Digital System Design</a></li>
                  <li><a class="dropdown-item" href="#">SATT</a></li>
                  <li><a class="dropdown-item" href="#">PTSP</a></li>
                </ul>
              </li>
            </ul>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false"> Year 3 </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#"> SEM 5 » </a>
                <ul class="submenu dropdown-menu">
                  <li><a class="dropdown-item" href="#">Aptitude</a></li>
                  <li><a class="dropdown-item" href="#">Control systems engineeing</a></li>
                  <li><a class="dropdown-item" href="#">Analog and Digital Communications</a></li>
                  <li><a class="dropdown-item" href="#">Computer Organisation and Architecture</a></li>
                  <li><a class="dropdown-item" href="#">Integrated Circuits and Applications</a></li>
                </ul>
              </li>
              <li><a class="dropdown-item" href="#"> SEM 6 » </a>
                
                <ul class="submenu dropdown-menu">
                 <li><a class="dropdown-item" href="#">MPMC</a></li>
                  <li><a class="dropdown-item" href="#">Digital Signal Processing</a></li>
                  <li><a class="dropdown-item" href="#">Computer Networks</a></li>
                  <li><a class="dropdown-item" href="#">AWP</a></li>
                  <li><a class="dropdown-item" href="#">Economics and Financing by for Engineers</a></li>
                </ul>
              </li>
            </ul>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false"> Year 4 </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#"> SEM 7 » </a>
                <ul class="submenu dropdown-menu">
                  <li><a class="dropdown-item" href="#">Subject 1</a></li>
                  <li><a class="dropdown-item" href="#">Subject 2</a></li>
                  <li><a class="dropdown-item" href="#">Subject 3</a></li>
                </ul>
              </li>
              <li><a class="dropdown-item" href="#"> SEM 8 » </a>
                
                <ul class="submenu dropdown-menu">
                  <li><a class="dropdown-item" href="#">Subject 1</a></li>
                  <li><a class="dropdown-item" href="#">Subject 2</a></li>
                  <li><a class="dropdown-item" href="#">Subject 3</a></li>
                </ul>
              </li>
            </ul>
          </li>



         
          

         
        </ul>
      </div>
    </div>
  </nav>


</body>

</html>
