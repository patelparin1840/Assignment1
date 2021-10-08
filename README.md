# 207_Assignment1
var fs = require('fs');
//create directory
fs.mkdir('Node.js',function(){

});

//remove directory
fs.rmdir('Node.js',function(){

});

//write file
fs.writeFile("myfiles.txt","This is for write file, This file made by parin patel",function(err){
    if(err)
    {
        console.log(err);
    }
    else
    {
        console.log("File Save Successfully..");
    }
});

//read file
fs.readFile("myfiles.txt","utf8",function(err,data){
    if(err)
    {
        console.log(err)
    }
    else
    {
        console.log(data);
    }
});

//Delete File

fs.unlink("myfiles.txt",function(err){
    if(err)
    {
        console.log(err);
    }
    else
    {
        console.log("File Deleted Successfully..");
    }
});

//Append data to file

fs.appendFile('myfiles.txt', 'Hello content!', function (err) {
    if(err)
    {
        console.log(err);
    }
    else
    {
        console.log("File Content Saved..");
    }
});

//Update/Replace file with new data

fs.readFile("myfiles.txt", 'utf8', function (err,data) {
    if (err) {
      return console.log(err);
    }
    //It will be replacing the word parin to a parin r  in a text file mytext.txt 
    var newValue = data.replace(/parin/, 'parin r ');
  
    fs.writeFile("myfiles.txt", newValue, 'utf8', function (err) {
       if (err)
       {
            return console.log(err);

       }
    });
  });

  //Rename File

  fs.rename('myfiles.txt','myfilesrename.txt',function(err){
    if(err)
    {
        console.log(err);
    }
    else
    {
        console.log("File name changed/rename..");
    }
})




