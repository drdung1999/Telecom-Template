<template>
  <div class="navigation absolute z-100 w-full">
    <div class="infor-bar w-full">
        <div class="wrap-infor-bar max-w-content m-auto flex align-center justify-between">
          <div class="left-bar flex">
            <i class="fa fa-facebook" aria-hidden="true"></i>
            <i class="fa fa-google-plus-official" aria-hidden="true"></i>
            <i class="fa fa-twitter-square" aria-hidden="true"></i>
            <i class="fa fa-instagram" aria-hidden="true"></i>
            <i class="fa fa-youtube" aria-hidden="true"></i>
          </div>
          <div class="right-bar flex">
            <p><a href="tel: (800) 323 456 897"><i class="fa fa-phone" aria-hidden="true"></i> (800) 323 456 897</a></p>
            <p><a href="mailto: info@sitename.com"><i class="fa fa-envelope" aria-hidden="true"></i> info@sitename.com</a></p>
            <p><a href=""><i class="fa fa-comments-o" aria-hidden="true"></i>Live Chat</a></p>
            <p><a href=""><i class="fa fa-question-circle" aria-hidden="true"></i>Support</a></p>
          </div>
        </div>
      </div>
      <div class="nav-bar w-full">
        <div class="wrap-nav-bar max-w-content m-auto flex align-center justify-between">
          <div class="left-nav flex">
            <img class="w-full logo" src="@/assets/images/logo.png" alt="" >
          </div>
          <div class="right-nav flex">'
            <ul class="flex align-center">
              <li class="active nav-btn"><a href="#">Home</a></li>
              <li class="relative nav-btn">
                <a href="#">About us <i class="fa fa-angle-down" aria-hidden="true"></i></a>
                <ul class="sub-menu absolute">
                  <li class="item"><a href="">Blog Left Sidebar</a></li>
                  <li class="item"><a href="">Blog Left Sidebar</a></li>
                  <li class="item"><a href="">Blog Right Sidebar</a></li>
                  <li class="item"><a href="">Blog No Sidebar</a></li>
                </ul>
              </li>
              <li class="relative nav-btn"><a href="#">Services</a></li>
              <li class="relative nav-btn">
                <a href="#">Blogs <i class="fa fa-angle-down" aria-hidden="true"></i></a>
                <ul class="sub-menu absolute">
                  <li class="item"><a href="">Blog Left Sidebar</a></li>
                  <li class="item"><a href="">Blog Left Sidebar</a></li>
                  <li class="item"><a href="">Blog Right Sidebar</a></li>
                  <li class="item"><a href="">Blog No Sidebar</a></li>
                </ul>
              </li>
              <li class="relative nav-btn">
                <a href="#">Contact us <i class="fa fa-angle-down" aria-hidden="true"></i></a>
                <ul class="sub-menu absolute">
                  <li class="item"><a href="">Blog Left Sidebar</a></li>
                  <li class="item"><a href="">Blog Left Sidebar</a></li>
                  <li class="item"><a href="">Blog Right Sidebar</a></li>
                  <li class="item"><a href="">Blog No Sidebar</a></li>
                </ul>  
              </li>
              <li class="relative"><i class="color-white pointer fa fa-search" aria-hidden="true"></i></li>
              <li class="relative mobile-bar"><i class="fa fa-bars color-white pointer" aria-hidden="true"></i></li>
            </ul>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.navigation {
  .infor-bar {
    background-color: rgba(21,21,21,.3);
    .wrap-infor-bar {
      color: var(--white);
      font-size: 0.9rem;
      padding: 5px 0;

      i {margin-right: 15px; font-size: 1rem;}

      .left-bar {
       i {font-size: 1.2rem; cursor: pointer;} 
      }

      .right-bar {
        i { color: var(--pink);}
        p { 
          margin-left: 30px;
          transition: 0.4s;
        }

        p:hover {
          i {color: var(--white);}
          a {color: var(--pink);}
        }
      }
    }
  }

  .nav-bar {
    .wrap-nav-bar {
      // .left-nav {}
      .right-nav {
        >ul {
          .mobile-bar {
            display: none;
          }
          >li {
            .sub-menu {
              background-color: var(--white);
              width: 220px;
              display: none;
              
              .item {
                > a{ display: inline-block; padding: 10px 10px; transition: 0.4s; color: black;}
              }
            }
              >a{
                padding: 45px 25px;
                display: inline-block;
                font-weight: 600;
                transition: 0.4s;
                display: flex;
                justify-content: center;
                align-items: center;

                i {margin-left: 10px;}
              }
              >i {
                padding: 0 25px;
                font-size: 1.5rem;
              }
          }

          .active {
            a {color: var(--pink); }
          }

          li:hover {
            >a, >i{color: var(--pink) !important; }

             .sub-menu {
               display: block;
             }
          }
        }
      }
    }
  }
}

@media (max-width: 1170px) {
}

@media (max-width: 915px) {
  .navigation {
    position: relative !important; 
    background-color: var(--purple) !important;
    .nav-bar {
      padding: 20px 0px;
      .mobile-bar {
        display: block !important;
        }
        .nav-btn {
          display: none !important;
        }
    }
    .wrap-infor-bar {
      font-size: 0.7rem !important;
      i {font-size: 0.8rem !important;}
    }
  }
}

@media (max-width: 700px) {
  .navigation {
    .infor-bar {
      padding: 12px 0 !important;
      .wrap-infor-bar {
        flex-direction: column !important;
        font-size: 1rem !important;
        i {font-size: 1rem !important;}
        .right-bar, .left-bar {
          flex-wrap: wrap !important;
          justify-content: space-around !important;
          p {margin-left: 5px !important; margin-right: 5px;}
        }
      }
    }
  }
}

@media (max-width: 415px) {
  .navigation {
    .infor-bar {
      .wrap-infor-bar {
        .left-bar {
          width: 100% !important;
        }
      }
    }
  }
}
</style>