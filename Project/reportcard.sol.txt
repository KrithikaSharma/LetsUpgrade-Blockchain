pragma solidity ^0.4.17 < 0.7.0;

contract  ReportCard{
    
    string public name;
    uint public rollno ;
    string public batch;
    int public mark1;
    int public mark2;
    int public mark3;
    int public mark4;
    //int sum=(mark1+mark2+mark3+mark4);
    //int result=(sum/400)*100;
    string public status;
    
    
    function ReportCard(string newName,uint newRollno, string newBatch, int newMark1, int newMark2, int newMark3, int newMark4, string newStatus) public{
        
        name=newName;
        rollno=newRollno;
        batch=newBatch;
        mark1=newMark1;
        mark2=newMark2;
        mark3=newMark3;
        mark4= newMark4;
        status= newStatus;
        if((mark1+mark2+mark3+mark4)/4 >= 35){
           status="Pass";
        }
        else{
           status="Fail";
        }
    }
    
    
    function getReportCardDetails() public view returns(string,uint,string,int,int,int,int,string){
        return(name,rollno,batch,mark1,mark2,mark3,mark4,status);
    }
}