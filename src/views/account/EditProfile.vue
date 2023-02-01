<script setup>
    import { ref } from 'vue'
    import CroppedImage from '../../components/global/CroppedImage.vue'
    import TextInput from '../../components/global/TextInput.vue'
    import DisplayCropperButton from '../../components/global/DisplayCropperButton.vue'
    import TextArea from '../../components/global/TextArea.vue'
    import CropperModal from '../../components/global/CropperModal.vue'
    import SubmitFormButton from '../../components/global/SubmitFormButton.vue'
    

    let firstName = ref(null)
    let lastName = ref(null)
    let location = ref(null)

</script>

<template>
    <div id="EditProfile" class="container max-w-4xl mx-auto pt-20 pb-20 px-6">
        <div class="text-gray-900 text-xl">Edit Profile</div>
        <div class="bg-green-500 w-full h-1"></div>

        <CropperModal />

        <div class="flex flex-wrap mt-4 mb-6">
            <div class="w-full md:w-1/2 px-3">
                <TextInput 
                    label="First Name"
                    placeholder="John"
                    v-model:input="firstName"
                    inputType="text"
                />
            </div>
            <div class="w-full md:w-1/2 px-3">
                <TextInput 
                    label="Last Name"
                    placeholder="Doe"
                    v-model:input="lastName"
                    inputType="text"
                />
            </div>
        </div>

        <div class="flex flex-wrap mt-4 mb-6">
            <div class="w-full md:w-1/2 px-3">
                <TextInput 
                    label="Location"
                    placeholder="Madrid, ES"
                    v-model:input="location"
                    inputType="text"
                />
            </div>
        </div>

        <div class="flex flex-wrap mt-4 mb-6">
            <div class="w-full md:w-1/2 px-3">
                <DisplayCropperButton
                    label="Profile Image"
                    btnText="Update Profile Image"
                    @showModal="showModal = true"
                />
            </div>
        </div>

        <div class="flex flex-wrap mt-4 mb-6">
            <div class="w-full md:w-1/2 px-3">
                <CroppedImage
                    label="Cropped Image"
                    :image="image"
                />
            </div>
        </div>

        <div class="flex flex-wrap mt-4 mb-6">
            <div class="w-full px-3">
                <TextArea
                    label="Description"
                    placeholder="Please enter some information here!!!"
                    v-model:description="description"
                />
            </div>
        </div>

        <div class="flex flex-wrap mt-8 mb-6">
            <div class="w-full px-3">
                <SubmitFormButton
                    btnText="Update Profile"
                    @click="updateUser"
                />
            </div>
        </div>
    
    
    </div>
</template>

