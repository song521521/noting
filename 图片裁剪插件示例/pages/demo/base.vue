<template>
	<view>
		<qf-image-cropper :width="500" :height="500" @crop="handleCrop"></qf-image-cropper>
	</view>
</template>

<script>
	import QfImageCropper from '@/uni_modules/qf-image-cropper/components/qf-image-cropper/qf-image-cropper.vue';
	export default {
		components: {
			QfImageCropper
		},
		methods: {
			handleCrop(e) {
				uni.previewImage({
					urls: [e.tempFilePath],
					current: 0
				});
				// console.log(e)
				// // #ifdef H5
				// h5下载图片
				// var a = document.createElement('a');
				// a.href = e.tempFilePath;
				// a.download = new Date().valueOf() + ".png";
				// a.click();
				// // #endif
				// // #ifndef H5
				// 非h5保存相册
				// uni.saveImageToPhotosAlbum({
				// 	filePath: e.tempFilePath,
				// 	success: () => {
				// 		uni.showToast({
				// 			title: '保存成功',
				// 			icon: 'success'
				// 		})
				// 	}
				// });
				// // #endif
			}
 		}
	}
</script>

<style>

</style>
