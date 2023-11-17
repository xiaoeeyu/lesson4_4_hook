function main(){
    Java.perform(function(){
        // // overloading with two parameters
        // Java.use("com.xiaoeryu.lesson4_4.MainActivity").fun.overload('int', 'int').implementation = function(arg1, arg2){
        //     var result = this.fun(100, 200);    // parameters can be changed
        //     console.log(Java.use("android.util.Log").getStackTraceString(Java.use("java.lang.Throwable").$new()));  // print call stack
        //     console.log("arg1, arg2, result", arg1, arg2, result);
        //     return result;
        // }
        // // overloading with a one parameter
        // Java.use("com.xiaoeryu.lesson4_4.MainActivity").fun.overload('java.lang.String').implementation = function(arg1){
        //     var result = this.fun(Java.use('java.lang.String').$new('NIHAO'));  // parameters can be changed
        //     console.log("arg1, result", arg1, result);
        //     return result;
        // }

        // Java.choose("com.xiaoeryu.lesson4_4.MainActivity",{
        //     onMatch:function(instance){
        //         console.log("found instance: ", instance)
        //         console.log("found instance: ", instance.secret())
        //     },onComplete:function(){}
        // })
        // var result = Java.use("com.xiaoeryu.lesson4_4.MainActivity").secret2();
        // console.log(result);

        Java.use("net.sqlcipher.database.SQLiteOpenHelper").getWritableDatabase.overload('java.lang.String').implementation = function(arg1){
            var result = this.getWritableDatabase(arg1);
            console.log(Java.use("android.util.Log").getStackTraceString(Java.use("java.lang.Throwable").$new()));
            console.log("arg1_str, result", arg1, result);
            return result;
        }
        Java.use("net.sqlcipher.database.SQLiteOpenHelper").getWritableDatabase.overload('[C').implementation = function(arg1){
            var result = this.getWritableDatabase(arg1);
            console.log("arg1_char, result", arg1, result);
            return result;
        }

    })
}

setImmediate(main)

function invoke(){
    Java.perform(function(){
        Java.choose("com.example.yaphetshan.tencentwelcome.MainActivity", {
            onMatch:function(instance){
                console.log("found instance ", instance);
                console.log("invoke instance.a ", instance.a());
            }, onComplete:function(){console.log("search completed!")}
        })
    })
}

setTimeout(invoke, 3000)
