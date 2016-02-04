# header 1

## header 2

### header 3

1. abc
2. efg
3. hij

* 1
* 2 
* 3

- 1
- 2 
- 3

> import

	/**
	 * 验证手机号码
	 * @param mobile
	 * @return
	 */
	public static boolean isMobileNO(String mobile) {
		boolean flag = false;
		try {
			Pattern p = Pattern.compile("^((13[0-9])|(147)|(15[^4,\\D])|(17[0-9])|(18[0-9]))\\d{8}$");
			Matcher m = p.matcher(mobile);
			flag = m.matches();
		} catch (Exception e) {
			flag = false;
		}
		return flag;
	}