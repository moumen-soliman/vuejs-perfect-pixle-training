<template>
  <header class="py-3">
    <div class="container">
      <div class="row flex-nowrap justify-content-between align-items-center">
        <div class="col-5 pt-1">
          <div class="text-muted boards">
            <img src="@/assets/icons/svg/rectangle.svg" alt="Nello Boards">
            <span>{{boards}}</span>
          </div>
        </div>
        <div class="main-logo col-2 text-center">
          <h4><b>{{logoBrand}}</b></h4>
        </div>
        <div class="search-part col-5 d-flex justify-content-end align-items-center">
          <a class="text-muted" href="#">
            <div class="input-group">
              <img src="@/assets/icons/svg/shape.svg" alt="Nello Search Icon">
              <input type="text" placeholder="Search …" class="form-control" aria-label="Text input with dropdown button">
            </div>
          </a>
          <div class="user-part">
            <button class="btn" type="button" @click="isHidden = !isHidden">
              <div class="user-part-details">
                <img src="https://avatars3.githubusercontent.com/u/24474287?s=460&v=4" :alt="`Nello - ${userInfo.name} Photo`"/>
                <span class="welcome-message">Hi</span>, <span class="user-name">{{userInfo.name}}</span>
              </div>
              <img src="@/assets/icons/svg/path-2.svg" alt="Nello Dropdown menu">
            </button>
            <div :class="isHidden ? 'dropdown-menu show' : 'dropdown-menu'">
              <button class="dropdown-item" type="button">Action</button>
              <button class="dropdown-item" type="button">Another action</button>
              <button class="dropdown-item" type="button">Something else here</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Navbar',
  props: ['userInfo'],
  data () {
    return {
      isHidden: false,
      boards: 'Boards',
      logoBrand: 'Nello.',
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
header {
  background: white;
  box-shadow: 0 5px 11px 0 rgba(0, 0, 0, 0.07);
  .row {
    padding: 15px 0;
    .main-logo {
      color: #7148fc;
      margin-top: 5px;
    }
    .boards {
      img {
        width: 24px;
        margin-top: -3px;
      }
      span {
        font-size: 15px;
        color: #999;
        margin: 9px;
      }
    }
    .search-part {
      img {
        width: 23px;
      }
      input {
        border: 0;
        font-style: italic;
        font-size: 16px;
        float: right;
        width: 9em;
        color: #999;
        opacity: 0.5;
        font-weight: 400;
      }
      .user-part {
        display: inline-block;
        .btn {
          font-size: 18px;
          color: black;
          padding: 0;
          background: none;
          img {
            width: 9px;
            margin-left: 9px;
          }
          .user-part-details {
            display: inline;
            .welcome-message {
              color: #834bc4;
              font-style: italic;
              font-weight: bold;
            }
            .user-name {
              white-space: nowrap;
              overflow: hidden;
              text-overflow: ellipsis;
              max-width: 4em;
              display: table-cell;
            }
            img {
              width: 38px;
              height: 38px;
              border-radius: 10px;
              margin-right: 2px;
            }
          }
        }
        .dropdown-menu {
          left: unset;
        }
      }
    }
  }
}
</style>
