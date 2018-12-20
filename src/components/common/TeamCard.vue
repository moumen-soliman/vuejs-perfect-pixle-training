<template>
  <div>
    <div class="team-card-dropdown col-12 text-center">
      <button class="btn" type="button" @click="isHidden = !isHidden">
        <div class="user-part-details">
          <div class="user-team-image text-center">
            <span><b>{{userInfo.team.charAt(0)}}</b></span>
          </div>
          <div class="user-team-info">
              <div>
                <span>{{userInfo.team}} Team</span>
                <img src="@/assets/icons/svg/path-2.svg" alt="Nello Dropdown menu">
              </div>
              <div>
                <span>{{userInfo.board}} Board</span>
              </div>
          </div>
          <div :class="isHidden ? 'dropdown-menu show' : 'dropdown-menu'">
            <button class="dropdown-item" type="button">Action</button>
            <button class="dropdown-item" type="button">Another action</button>
            <button class="dropdown-item" type="button">Something else here</button>
          </div>
        </div>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamCard',
  props: ['userInfo'],
  data () {
    return {
      isHidden: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss"scoped>
.team-card-dropdown {
  display: inline-flex;

  .btn {
    padding: 16px 51px;
    border-radius: 10px;
    background-color: #f0f0f0;
    margin: 40px auto;

    img {
      width: 11px;
      margin-left: 9px;
    }

    .user-part-details {
      display: inline;

      .user-team-info {
        display: inline-block;
        text-align: left;

        div:first-child {
          span {
            font-size: 21px;
          }
        }

        div:last-child {
          margin-top: -3px;

          span {
            font-size: 15px;
            color: #bababa;
          }
        }
      }

      .user-team-image {
        display: inline-block;
        width: 52px;
        height: 52px;
        border-radius: 10px;
        background-color: #7148fc;
        color: white;
        padding: 6px;
        margin-right: 12px;
        float: left;

        span {
          margin: auto;
          font-size: 24px;
        }
      }
    }
  }

  .dropdown-menu {
    left: unset;
    top: 75%;
  }
}

</style>
