//4.英文变中文
        //第一种：
        var data = {
             "uactpvalue": {
                    "oneButton": "27.11",
                    "other": "20",   
                    "message": "12.23",
                    "account": "60.66"
             }
        };
        var arr = [];
        var len = ['oneButton','other','message','account'];
        var legend =[];
        var legend = ['一键登录','第三方登录','短信验证码登录','账号登录'];
        let a = [{e:'oneButton',z:'一键登录'},{e:'other',z:'第三方登录'},{e:'message',z:'短信验证码登录'},{e:'account',z:'账号登录'}]
        a.forEach(i=>{
         arr.push({name:i.z,value:data.uactpvalue[i.e]})
        })
        console.log(arr)

        //第二种：
        data.uactpvalue = {
            "一键登录": data.uactpvalue.oneButton,
            "第三方登录": data.uactpvalue.other,
            "短信验证码登录": data.uactpvalue.message,
            "账号登录": data.uactpvalue.account
        };

        for(var i in data.uactpvalue){
            //console.log(i);
            arr.push({
                name:i,
                value:data.uactpvalue[i]
            })
        }
