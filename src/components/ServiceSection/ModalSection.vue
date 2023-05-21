<script setup>
  import { onMounted, ref } from "vue";
  import { Modal } from "bootstrap";
  defineProps({
    title: {
      type: String,
      default: "<<Title goes here>>",
    },
    paragraphs: Array,
    lists: Array,
    addresses: Array,
    link: Object
  });
  
  let modalEle = ref(null);
  let thisModalObj = null;

  onMounted(() => {
    thisModalObj = new Modal(modalEle.value);
  });
  function _show() {
    thisModalObj.show();
  }
  defineExpose({ show: _show });
</script>

<template>
  <!-- Modal -->
  <div class="modal fade" id="exampleModal" tabindex="-1" aria-hidden="true" ref="modalEle">
    <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="staticBackdropLabel">{{ title }}</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <!-- electronic waste deposit -->
          <p v-if="lists">{{ paragraphs[0] }}</p>
          <ul v-if="lists">
            <li 
              v-for="list in lists" 
              :key="list"
            >
              <i class="bi bi-check-circle"></i>
              <span class="title">{{ list.title }}</span>
              <span>{{ list.text }}</span>
            </li>
          </ul>
          <p v-if="lists">{{ paragraphs[1] }}</p>

          <p v-if="lists">{{ paragraphs[2] }}</p>

          <ul v-if="lists">
            <li 
              v-for="address in addresses" 
              :key="address"
            >
              <span>
                  <i class='bx bx-building'></i>
                  <span class="title">{{ address.title }}</span> 
                  {{ address.text }}
              </span>
              <span class="d-block">
                <i class='bx bx-map' ></i>
                <span class="title">Endereço: </span>  
                {{ address.address }}
              </span>
              <span class="d-block">
                <i class='bx bx-phone' ></i>
                <span class="title">Telefone: </span> 
                {{ address.phone }}
              </span>
              <hr>
            </li>
          </ul>

          <!-- footprint calculator -->
          <p v-show="!lists" 
            v-for="paragraph in paragraphs" 
            :key="paragraph"
          >
            {{ paragraph }}
          </p>

          <a :href="link.link" target="_blank" v-if="link">
            <i class='bx bx-link-external' ></i>
            <span class="title">{{ link.text }}</span>
          </a>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fechar</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .modal-dialog-scrollable .modal-content {
    overflow-y: auto;
  }

  .modal-dialog {
    max-width: 800px;
  }

  ul {
    list-style: none;
    padding: 0;
  }

  ul li {
    padding-bottom: 10px;
  }

  i {
    font-size: 20px;
    padding-right: 4px;
    color: #16df7e;
  }

  .title {
    color: #16df7e;
  }
</style>