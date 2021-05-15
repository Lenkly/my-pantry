<template>
  <div id="modal">
    <div class="modal-container">
              <div class="modal-header">
                <h3>
                  {{ heading }}
                </h3>
              </div>

              <div class="modal-body">
                <p>
                  {{ description }}
                </p>
              </div>

              <div class="modal-footer">
                <p>
                  {{ details }}
                  <button class="modal-default-button" v-on:click="$emit('close')">
                    OK
                  </button>
                </p>
              </div>
            </div>
            </div>
</template>

<script>
export default {
    name: 'Modal',
    props: {
        heading: String,
        description: String,
        details: String
    }
}
</script>

<style>

.modal-container {
  width: 80vw;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.modal-header h3 {
  margin-top: 0;
  color: #42b983;
}

.modal-body, .modal-footer {
  margin: 20px 0;
}

/* 


.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
} */

</style>