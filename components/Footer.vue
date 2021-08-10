<template>
  <footer class="w-full">
    <div class="footer-cloud w-full"><img class="w-full" src="@/assets/images/footer-clouds.png" alt=""></div>
    <div class="wrap-footer max-w-content m-auto">
      <div class="wrap-item grid w-full">
        <div class="item">
          <div class="col-title" style="font-weight:700;">TELECOM</div>
          <p>Street 238,52 tempor Donec ultricies mattis nulla, suscipit risus tristique ut.</p>
          <p>Phone: 1.800.555.6789</p>
          <p>Email: <a href="mailto:support@sitename.com"> support@sitename.com</a></p>
          <p>Web: <a href="aabadsabsa.net"> aabadsabsa.net</a></p>
        </div>
        <div class="item">
           <div class="col-title" >Quick links</div>
           <p class="active"><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>Home</a></p>
           <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>About Us</a></p>
           <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>Services</a></p>
           <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>Blogs</a></p>
           <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>Contact Us</a></p>
        </div>
        <div class="item">
          <div class="col-title" >Our Services</div>
          <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>VoIP for Business</a></p>
          <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>Call Center Software</a></p>
          <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>Hosted PBX</a></p>
          <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>VoIP for Home</a></p>
          <p><a href=""><i class="fa fa-angle-right" aria-hidden="true"></i>Cloud SSD</a></p>
        </div>
        <div class="item">
          <div class="col-title" >Newsletter</div>
            <form>
              <input type="text">
              <i class="fa fa-paper-plane" aria-hidden="true"></i>
            </form>
            <div class="social-icons flex align-center">
              <div class="icon"><i class="fa fa-facebook-square" aria-hidden="true"></i></div>
              <div class="icon"><i class="fa fa-twitter" aria-hidden="true"></i></div>
              <div class="icon"><i class="fa fa-instagram" aria-hidden="true"></i></div>
              <div class="icon"><i class="fa fa-medium" aria-hidden="true"></i></div>
              <div class="icon"><i class="fa fa-behance" aria-hidden="true"></i></div>
              <div class="icon"><i class="fa fa-google-plus-official" aria-hidden="true"></i></div>
            </div>
        </div>
      </div>
    </div>
    <div class="copyright w-full">
      <div class="wrap-copyright max-w-content m-auto flex justify-between">
        <p>© 2020 Telecom. All Rights Reserved.</p>
        <p>Design by Unitech Themes</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss">
footer {
  background-image: url("@/assets/images/footer-bg.jpg");
  background-size: cover;
  min-height: 500px;
  height: auto;
  .wrap-footer {
    .wrap-item {
      grid-template-columns: 1fr 1fr 1fr 1fr;
      gap: 20px;
      padding: 40px 0px;
      .item { 
        color: var(--white-2);
        i {margin-right: 10px;}
        .active {a {color: var(--pink);}}
        .col-title {
          color: var(--white);
          font-size: 1.2rem;
          padding-bottom: 25px;
          border-bottom: 1px solid #4e2e72;
          position: relative;
          margin-bottom: 35px;
        }
        .col-title::after {
          content: "";
          display: block;
          height: 1px;
          position: absolute;
          bottom: -1px;
          width: 40px;
          left: 0;
          background-color: var(--dark-pink);
        }

        .social-icons {
          margin-top: 40px;
          padding-top: 20px;
          border-top: solid 1px #484246;
          border-color: rgba(78,46,114, 0.4);
          .icon {
            cursor: pointer;
            transition: 0.4s;
            padding: 7px;
            background-color: #141414;
            border-radius: 5px;
            margin-right: 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            i {color: var(--white); margin: 0px; padding: 0px;}
          }
          .icon:hover { 
            background-color: var(--bg-white);
            i {color: var(--pink);}
          }
        }
        form {
          position: relative;
          input {
            padding: 11px 13px;
            border-radius: 5px;
            width: 100%;
          }
          i {
            position: absolute;
            font-size: 1.4rem;
            top: 50%;
            transform: translateY(-50%);
            color: white;
            padding: 8px 10px;
            right: 0;
            background-color: black;
            border-radius: 5px;
            margin-right: 3px !important;
          }
        }
      }
      .item:nth-child(1) {a {color: var(--pink);}}
      .item:nth-child(2) p a, .item:nth-child(3) p a {
        transition: 0.4s;
      }
      .item:nth-child(2) p:hover, .item:nth-child(3) p:hover {
        a {color: var(--dark-pink);}
      }
    }
  }
  .copyright {
    padding: 10px 0px;
    color: var(--white);
    background-color: rgba(0,0,0, 0.3);
  }
}

@media (max-width: 750px) {
  footer {
    .wrap-item {grid-template-columns: 1fr !important;}
    .wrap-copyright.max-w-content.m-auto.flex.justify-between {
      flex-direction: column;
      text-align: center;
    }
  }
}

@media (max-width: 415px) {

}
</style>