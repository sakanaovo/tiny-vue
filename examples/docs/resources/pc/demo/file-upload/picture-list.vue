<template>
  <tiny-file-upload :action="action" :file-list="fileList" list-type="picture">
    <tiny-button type="primary">点击上传</tiny-button>
  </tiny-file-upload>
</template>

<script lang="jsx">
import { FileUpload, Button } from '@opentiny/vue'

export default {
  components: {
    TinyFileUpload: FileUpload,
    TinyButton: Button
  },
  data() {
    return {
      action: 'http://localhost:3000/api/upload',
      imageUrl: '',
      fileList: [
        {
          name: 'test1',
          url: 'static/images/fruit.jpg'
        },
        {
          name: 'test2',
          url: 'static/images/book.jpg'
        }
      ]
    }
  }
}
</script>
