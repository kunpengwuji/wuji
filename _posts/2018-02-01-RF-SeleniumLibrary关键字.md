---
published: false
---
## 关键字

RF SeleniumLibrary的关键字就是封装好的函数，围绕着Selenium在Web某个方面的功能会提供多个关键字，这些关键字被封装在该功能的Keywords类里，如ElementKeywords类封装了所有与element功能相关的关键字。

在这个库的docs文件夹中可以找到所有关键字按字母排序的说明文档，下面列出的是src文件夹下各个功能keywords所包含的关键字，具体使用某一个关键字时可根据函数名查找说明文档。

## alert.py
类-AlertKeywords
方法-
1. input_text_into_alert(self, text, action=ACCEPT, timeout=None)
1. alert_should_be_present(self, text='', action=ACCEPT, timeout=None)
1. alert_should_not_be_present(self, action=ACCEPT, timeout=0)
1. handle_alert(self, action=ACCEPT, timeout=None)

## browsermanagement.py
类-BrowserManagementKeywords
方法-
1. close_all_browsers(self)
1. close_browser(self)
1. open_browser(self, url, browser='firefox', alias=None,
1.                      remote_url=False, desired_capabilities=None,
1.                      ff_profile_dir=None)
1. create_webdriver(self, driver_name, alias=None, kwargs={}, **init_kwargs)
1. switch_browser(self, index_or_alias)
1. get_source(self)
1. get_title(self)
1. get_location(self)
1. location_should_be(self, url)
1. location_should_contain(self, expected)
1. log_location(self)
1. log_source(self, loglevel='INFO')
1. log_title(self)
1. title_should_be(self, title)
1. go_back(self)
1. go_to(self, url)
1. reload_page(self)
1. get_selenium_speed(self)
1. get_selenium_timeout(self)
1. get_selenium_implicit_wait(self)
1. set_selenium_speed(self, value)
1. set_selenium_timeout(self, value)
1. set_selenium_implicit_wait(self, value)
1. set_browser_implicit_wait(self, value)

## cookie.py
类-CookieKeywords
方法-
1. delete_all_cookies(self)
1. delete_cookie(self, name)
1. get_cookies(self)
1. get_cookie(self, name)
1. add_cookie(self, name, value, path=None, domain=None, secure=None, expiry=None)

## element.py
类-ElementKeywords
方法-
1. get_webelement(self, locator)
1. get_webelements(self, locator)
1. element_should_contain(self, locator, expected, message=None)
1. element_should_not_contain(self, locator, expected, message=None)
1. page_should_contain(self, text, loglevel='INFO')
1. page_should_contain_element(self, locator, message=None, loglevel='INFO', limit=None)
1. page_should_not_contain(self, text, loglevel='INFO')
1. page_should_not_contain_element(self, locator, message=None, loglevel='INFO')
1. assign_id_to_element(self, locator, id)
1. element_should_be_disabled(self, locator)	
1. element_should_be_enabled(self, locator)
1. element_should_be_focused(self, locator)
1. element_should_be_visible(self, locator, message=None)
1. element_should_not_be_visible(self, locator, message=None)
1. element_text_should_be(self, locator, expected, message=None)
1. get_element_attribute(self, locator, attribute=None)
1. get_horizontal_position(self, locator)
1. get_element_size(self, locator)
1. get_value(self, locator)
1. get_text(self, locator)
1. clear_element_text(self, locator)
1. get_vertical_position(self, locator)
1. click_element(self, locator)
1. click_element_at_coordinates(self, locator, xoffset, yoffset)
1. double_click_element(self, locator)
1. set_focus_to_element(self, locator)
1. focus(self, locator)
1. drag_and_drop(self, locator, target)
1. drag_and_drop_by_offset(self, locator, xoffset, yoffset)
1. mouse_down(self, locator)
1. mouse_out(self, locator)
1. mouse_over(self, locator)
1. mouse_up(self, locator)
1. open_context_menu(self, locator)
1. simulate_event(self, locator, event)
1. simulate(self, locator, event)
1. press_key(self, locator, key)
1. click_link(self, locator)
1. get_all_links(self)
1. mouse_down_on_link(self, locator)
1. page_should_contain_link(self, locator, message=None, loglevel='INFO')
1. page_should_not_contain_link(self, locator, message=None, loglevel='INFO')
1. click_image(self, locator)
1. mouse_down_on_image(self, locator)
1. page_should_contain_image(self, locator, message=None, loglevel='INFO')
1. page_should_not_contain_image(self, locator, message=None, loglevel='INFO')
1. get_element_count(self, locator)
1. add_location_strategy(self, strategy_name, strategy_keyword, persist=False)
1. remove_location_strategy(self, strategy_name)

## formelement.py
类-FormElementKeywords
方法-
1. submit_form(self, locator=None)
1. checkbox_should_be_selected(self, locator)
1. checkbox_should_not_be_selected(self, locator)
1. page_should_contain_checkbox(self, locator, message=None, loglevel='INFO')
1. page_should_not_contain_checkbox(self, locator, message=None, loglevel='INFO')
1. select_checkbox(self, locator)
1. unselect_checkbox(self, locator)
1. page_should_contain_radio_button(self, locator, message=None, loglevel='INFO')
1. page_should_not_contain_radio_button(self, locator, message=None, loglevel='INFO')
1. radio_button_should_be_set_to(self, group_name, value)
1. radio_button_should_not_be_selected(self, group_name)
1. select_radio_button(self, group_name, value)
1. choose_file(self, locator, file_path)
1. input_password(self, locator, password)
1. input_text(self, locator, text)
1. page_should_contain_textfield(self, locator, message=None, loglevel='INFO')
1. page_should_not_contain_textfield(self, locator, message=None, loglevel='INFO')
1. textfield_should_contain(self, locator, expected, message=None)
1. textfield_value_should_be(self, locator, expected, message=None)
1. textarea_should_contain(self, locator, expected, message=None)
1. textarea_value_should_be(self, locator, expected, message=None)
1. click_button(self, locator)
1. page_should_contain_button(self, locator, message=None, loglevel='INFO')
1. page_should_not_contain_button(self, locator, message=None, loglevel='INFO')









