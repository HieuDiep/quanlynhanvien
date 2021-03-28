<template>
    <div id="customerclick" class="dialog dialog-hide">
        <div class="model"></div>
        <div class="dialog-content">
            <div class="dialog-header">
                <div class="dialog-title">THÔNG TIN KHÁCH HÀNG</div>
                <div class="dialog-close-button" @click="closeForm">&#x2715;</div>
            </div>
            <div class="dialog-body" >
                <div class="body-top">
                    <div class="avatar">
                        <div class="photo">
                            <img src="../../assets/img/default-avatar.jpg" alt="" class="img">
                        </div>
                        <div class="text">
                            <p>Vui lòng chọn ảnh có định dạng</p> 
                            <b>.jpg .jpeg .png .gif</b>
                        </div>
                    </div>
                    
                    <div class="form">
                        <div class="form-input">
                            <label for="">Mã khách hàng (*)</label>
                            <input type="text" class="input">
                        </div>
                        
                        <div class="form-input">
                            <label for="">Mã thẻ thành viên</label>
                            <input type="text" class="input">
                        </div>
                        
                        <div class="form-input">
                            <label for="">Ngày sinh</label>
                            <input type="date" class="input">
                        </div>
                        
                    </div> 
                    <div class="form">
                        <div class="form-input">
                            <label for="">Họ và tên (*)</label>
                            <input type="text" id="txtCustomername" class="input">
                        </div>
                        <div class="form-input">
                            <label for="">Nhóm khách hàng</label>
                           <select id="cbCustomerGroup" class="input">
                            <option value="0cb5da7c-59cd-4953-b17e-c9adc9161663">Nhóm khách hàng MISA</option>
                            <option value="19165ed7-212e-21c4-0428-030d4265475f">Khách VIP</option>
                            <option value="3631011e-4559-4ad8-b0ad-cb989f2177da">Khách vãng lai</option>
                            <option value="7a0b757e-41eb-4df6-c6f8-494a84b910f4">Khách thường</option>
                        </select>
                        </div>
                        <div class="form-input">
                            <label for="" class="check-box">Giới tính</label> <br>
                                <input type="radio" id="male" name="gender" value="male">
                                <label for="male">Nam</label>
                                <input type="radio" id="female" name="gender" value="female">
                                <label for="female">Nữ</label>
                                <input type="radio" id="other" name="gender" value="other">
                                <label for="other">Khác</label>
                        </div>
                    </div>
                </div>
                <div class="dialog-down">
                    <div class="form-2">
                        <div class="form-21">
                            <label for="">Email</label>
                            <input type="text" class="input input2" placeholder="example@domain.com">
                        </div>
                        <div class="form-22">
                            <label for="">Số điện thoại (*)</label>
                            <input type="text" class="input input3">
                        </div>
                        
                    </div>
                    <div class="form-2">
                        <div class="form-21">
                            <label for="">Tên công ty</label>
                            <input type="text" class="input input2">
                        </div>
                        <div class="form-22">
                            <label for="">Mã số thuế</label>
                            <input type="text" class="input input3" placeholder="Mã số thuế của công ty">
                        </div>
                    </div>
                    <div class="form-2">
                        <div class="form-21">
                            <label for="">Địa chỉ</label>
                        <input type="text" class="input input4">
                        </div>
                    </div>
                </div>
            </div>  
            <div class="dialog-footer">
                <div class="button2">
                    <button class="bnt-inactive" @click="closeForm">Hủy</button>
                    <button id="btnSave" class="btn-default">Lưu</button>
                </div>
                
            </div>
        </div>
    </div>
</template>
<script>
export default {
    
    methods:{
        closeForm(){
            this.$emit('close');
        }
    }
}
</script>
<style scoped>
@import url('../../style/base/dialog.css');


</style>