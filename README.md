# connect_web_server
connect your flutter app to web server

what is server? file server, Http server, Database server, Dns Server

HTTP: Hyper text transfer protocol

http is the underlying protocol used by the world wide web and this protocol defines how messages are formatted and transmitted, and what actions web servers and browsers should take in response to various commands.

Future in dart is generic and help us to do lists in the same time and don't return anythings just do somethings

Future<void> cleanRoom(){
    print('cleanRooms');
    return Future.delayed(Duration(seconds:3));
}

Async Programming
use Future and async fo run a function in the future

void main() async{

    String fullName = await getDateFromServer();
    print('data is: $fullName');

    # or

    getDateFromServer().then((value) => print('data is: $fullName'))

    also you can catch error

    getDateFromServer().then((value) => print('data is: $fullName')).catchError((e){
        print('error is throw: $e')
    });



}


Future<String> getDataFromServer(){
    
    return Future.delayed(Duration(second:2)).then((value)=> ' Elias');

    also you can catch error

    return Future.delayed(Duration(second:2)).then((value)=> throw Exception('async test'));
}