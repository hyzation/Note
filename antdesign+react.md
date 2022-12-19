# antdesign+react
## 安装 
官中文档 https://ant.design/docs/react/introduce-cn
## 表单+验证
```
<Form>
    <Form.Item label="联系方式" name='contactBus'
        rules={[
        {
            required: true,
            message: '联系方式不能为空',
        },
        {
            pattern: /^(13[0-9]|14[01456879]|15[0-35-9]|16[2567]|17[0-8]|18[0-9]|19[0-35-9])\d{8}$/,
            message: '请正确输入手机号',
        },
        ]}
    >
        <Input autoComplete={"off"} />
    </Form.Item>
    <Form.Item>
        <Button type="primary" onClick={submit} htmlType="submit">提交</Button>
    </Form.Item>
</Form>

//获取表单值
let contact = carouselEL.current.getFieldsValue().contactBus
```
