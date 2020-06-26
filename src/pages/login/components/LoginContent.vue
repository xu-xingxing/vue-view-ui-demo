<template>
	<div class="login-content">
		<Row type="flex" justify="center">
			<Col span="8" style="height: 600px;">
				<Layout>
					<Content style="display: flex;justify-content: center;background: #eee;">
						<Card class="card">
							<br />
							<h1 style="text-align: center;font-size: 32px;">欢迎登录</h1>
							<br />
							<Divider />
							<br />
							<Form ref="formValidate" :model="formValidate" :rules="ruleValidate" :label-width="80">
								<FormItem label="用户名" prop="name">
									<Input v-model="formValidate.name" placeholder="请输入用户名"></Input>
								</FormItem>
								<FormItem label="密码" prop="password">
									<Input v-model="formValidate.password" placeholder="请输入密码"></Input>
								</FormItem>
								</FormItem>
								<FormItem label="Staus" prop="status">
									<RadioGroup v-model="formValidate.status">
										<Radio label="before">仅前端</Radio>
										<Radio label="behind">发送给后端</Radio>
									</RadioGroup>
								</FormItem>
                <FormItem v-show="formValidate.status === 'behind'" label="IP地址" prop="ip">
                  <Input v-model="formValidate.ip"></Input>
								</FormItem>
								<FormItem>
									<Button type="primary" @click="handleSubmit('formValidate')">Submit</Button>
									<Button @click="handleReset('formValidate')" style="margin-left: 8px">Reset</Button>
								</FormItem>
							</Form>
						</Card>
					</Content>
				</Layout>
			</Col>
		</Row>
	</div>
</template>

<script>
export default {
  name: 'LoginContent',
  data () {
    return {
      formValidate: {
        name: '',
        password: '',
        status: 'before',
        ip: 'http://192.168.101.55'
      },
      ruleValidate: {
        name: [
            { required: true, message: 'The name cannot be empty', trigger: 'blur' }
        ],
        password: [
            { required: true, message: 'Mailbox cannot be empty', trigger: 'blur' },
            { type: 'email', message: 'Incorrect email format', trigger: 'blur' }
        ],
        ip: [
           { required: true, message: '后端ip地址不能为空', trigger: 'blur'}
        ],
        status: [
            { required: true, message: 'Please select gender', trigger: 'change'}
        ] 
      }
		}
	},
    methods: {
      handleSubmit(name) {
        this.$refs[name].validate((valid) => {
          if (valid) {
            this.$Message.success(`用户名：'${this.formValidate.name},密码： ${this.formValidate.password}`)
          } else {
            this.$Message.error('格式错误，请检查')
          }
        })
      },
      handleReset(name) {
        this.$refs[name].resetFields()
      }
  	}
}
</script>

<style lang="stylus" scoped>
.card {
	border-radius: 30px;
	width: 370px;
	box-shadow: 5px 5px 5px #ccc;

	.border-2px {
		border: 2px solid #ddd;
	}
}

.Form {
	padding: 5%;
}
</style>