<template>
  <div>
    <div id="form-input">
      <div class="row">
        <div class="col">
          <h2 style="font-weight: 700">Review</h2>
        </div>

        <div class="col">
          <b-form-rating
            v-model="star"
            variant="warning"
            class="mb-2"
            style="border: hidden"
          ></b-form-rating>
        </div>
      </div>

      <form style="margin-top: 10px">
        <input
          class="form-control"
          type="text"
          placeholder="Tulis nama kamu"
          v-model="name"
        /><br />

        <textarea
          class="form-control"
          id="textArea"
          rows="3"
          placeholder="Tulis review terbaikmu"
          v-model="review"
        ></textarea
        ><br />

        <div class="row">
          <div class="col">
            <input type="file" id="file" accept="image/*" />
            <label for="file"> Upload Gambar </label>
          </div>

          <div class="col-align-right" style="margin-right: 15px">
            <button type="submit" class="btn btn-primary">Kirim</button>
          </div>
        </div>
      </form>
    </div>

    <!-- show data -->
    <div id="show-data">
      <hr />
      <div class="card">
        <div class="card-body">
          <div class="card-title">
            <div class="row">
              <div class="col" style="margin-left: 1%">
                <p>Name : {{ name }}</p>
              </div>
              <div class="col">
                <p>with {{ star }} <i class="fa fa-star"></i></p>
              </div>
              <div class="col-align-right" style="margin-right: 20px">
                <div>
                  <b-dropdown size="sm" class="m-2">
                    <b-dropdown-item-button size="sm">Edit</b-dropdown-item-button>
                    <b-dropdown-item-button size="gitsm">Delete</b-dropdown-item-button>
                  </b-dropdown>
                </div>
              </div>
            </div>
          </div>
          <div class="row" style="margin-left: 1%">
            <p>Review : {{ review }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script src="https://cdn.jsdelivr.net/npm/vue@2.5.16/dist/vue.js"></script>

<script>
export default {
  data() {
    return {
      name: "",
      star: "",
      review: "",
    };
  },
};
</script>

<style>
</style>