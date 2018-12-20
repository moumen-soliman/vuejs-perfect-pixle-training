<template>
  <header class="blog-header py-3">
    <div class="container">
      <div class="row flex-nowrap justify-content-between align-items-center">
        <div class="col-4 pt-1">
          <div class="text-muted boards">
            <img src="@/assets/icons/svg/rectangle.svg" alt="Nello Boards">
            <span>{{boards}}</span>
          </div>
        </div>
        <div class="main-logo col-4 text-center">
          <h4><b>{{logoBrand}}</b></h4>
        </div>
        <div class="search-part col-4 d-flex justify-content-end align-items-center">
          <a class="text-muted" href="#">
            <div class="input-group">
              <img src="@/assets/icons/svg/shape.svg" alt="Nello Search Icon">
              <input type="text" placeholder="Search …" class="form-control" aria-label="Text input with dropdown button">
            </div>
          </a>
          <div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenu2" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown
  </button>
  <div class="dropdown-menu" aria-labelledby="dropdownMenu2">
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
  name: 'Home',
  data () {
    return {
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
    }
  }
}
</style>
