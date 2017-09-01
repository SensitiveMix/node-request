```bash
                                                                                 __ 
  _____   _____   ____ ___           _____  ___   ____ _  __  __  ___    _____  / /_
 / ___/  / ___/  / __ `__ \ ______  / ___/ / _ \ / __ `/ / / / / / _ \  / ___/ / __/
/ /__   / /     / / / / / //_____/ / /    /  __// /_/ / / /_/ / /  __/ (__  ) / /_  
\___/  /_/     /_/ /_/ /_/        /_/     \___/ \__, /  \__,_/  \___/ /____/  \__/  
                                                  /_/                               
```
[![Standard - JavaScript Style Guide](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)
[![Build Status](https://travis-ci.org/SensitiveMix/node-tim.svg?branch=master)](https://travis-ci.org/SensitiveMix/node-tim)

## Installation
```
yarn add crm-request
```

## Options
Initialize Tim plugin with the given options.

```JavaScript
crm_request(access_token, { host: "", protocol: "" })
```
Options:

 - `access_token` 用户通过Teambition Account授权获取到的token, 用于验证请求是否合法并经过用户授权
 - `host` 非必需参数, 指定API地址s


## Usage

* callback
```JavaScript
let accessToken = 'crm accessToken'
let crm = new crm_request(accessToken)

crm.get('/users/me', (err, data) => {
  // user's profile
  if (err) throw err
  console.log(data)
})

```

* promise
```JavaScript
let accessToken = 'crm accessToken'
let crm = new crm_request(accessToken)
crm
  .get('/users/me')
  .then(userprofile => console.log(userprofile))
  .catch(err => console.error(err))
```

## License

ISC License

Copyright (c) 2017
