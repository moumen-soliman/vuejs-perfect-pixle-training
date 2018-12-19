<template>
  <div>
    <div class="d-flex flex-column flex-md-row align-items-center mb-3 ">
      <nav class="my-2 my-md-0 mr-md-3">
        <a class="navbar-brand my-0 mr-md-auto font-weight-normal" href="#">
          <img
            src="@/assets/images/home/png-icons/seen-logo.png"
            srcset="@/assets/images/home/png-icons/seen-logo@2x.png 2x,
            @/assets/images/home/png-icons/seen-logo@3x.png 3x"
            class="d-inline-block align-top"
            alt="Sceen Logo"
          >
        </a>
        <ul>
          <li><a class="p-2" href="#">تواصل معنا</a></li>
          <li>
            <a class="btn btn-outline-primary" href="#">
              الملف التعريفي
              <img
                  src="@/assets/images/home/png-icons/cloud-storage-download.png"
                  srcset="@/assets/images/home/png-icons/cloud-storage-download@2x.png 2x,
                  @/assets/images/home/png-icons/cloud-storage-download@3x.png 3x"
                  alt="sceen-cloud-storage-dodwnload"
              />
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar'
};
</script>

<style lang="scss">
nav {
  width: 100%;
  padding: 38px 0;
  ul {
    float: left;
    padding: 0;
    li {
      display: inline-block;
      list-style: none;
      margin-right: 36px;
      a {
        color: white;
        font-size: 14px;
        &:hover {
          text-decoration: none;
          color: white;
        }
        &.btn {
          width: 145px;
          height: 40px;
          border-radius: 20px;
          background-color: #1f9eab;
          color: white;
          border: 0;
          font-size: 14px;
          &:hover {
            opacity: 0.8;
            background-color: #1f9eab;
          }
          img {
            width: 20px;
            height: 15px;
            object-fit: contain;
            margin-left: 7px;
          }
        }
      }
    }
  }
  .navbar-brand {
    img {
      width: 120px;
      object-fit: contain;
      margin-top: 10px;
    }
  }
}
</style>
