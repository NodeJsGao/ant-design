---
order: 3
title: 触发事件
---

点击菜单项后会触发事件，用户可以通过相应的菜单项 key 进行不同的操作。

````jsx
import { Menu, Dropdown, Icon } from 'antd';
const onClick = function ({ key }) {
  console.log(`点击了菜单${key}`);
};

const menu = (
  <Menu onClick={onClick}>
    <Menu.Item key="1">第一个菜单项</Menu.Item>
    <Menu.Item key="2">第二个菜单项</Menu.Item>
    <Menu.Item key="3">第三个菜单项</Menu.Item>
  </Menu>
);

ReactDOM.render(
  <Dropdown overlay={menu}>
    <a className="ant-dropdown-link" href="#">
      鼠标移入，点击菜单 <Icon type="down" />
    </a>
  </Dropdown>
, mountNode);
````
