unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls;

type
  TForm1 = class(TForm)
    btn1: TButton;
    mmo1: TMemo;
    edt1: TEdit;
    procedure btn1Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.dfm}

procedure TForm1.btn1Click(Sender: TObject);
var
  r:Cardinal;
  q:Cardinal;
  t:Cardinal;
  s:Cardinal;
  countDecision:Cardinal;

  str1:string;
  str1Num:Integer;
  str2:string;
  str2Num:Integer;
  rez:string;
  rezNum:Integer;
begin
  countDecision:=0;
  str1:='';
  r:=1;
  while r<=9 do
  begin
    t:=0;
    while t<=9 do
    begin
      q:=0;
      while q<=9 do
      begin
        s:=1;
        while s<=9 do
        begin
          str1:=IntToStr(r)+IntToStr(t)+IntToStr(r)+IntToStr(q);
          str1Num:=StrToInt(str1);

          str2:=IntToStr(r)+IntToStr(q)+IntToStr(r)+IntToStr(s);
          str2Num:=StrToInt(str2);

          rez:=IntToStr(s)+IntToStr(t)+IntToStr(s)+IntToStr(s);
          rezNum:=StrToInt(rez);


          if str1Num+str2Num=rezNum then
          begin
            Form1.mmo1.Lines.Add(str1+'+'+str2+'='+rez+'<->'+
            intTostr(str1Num+str2Num)+'='+rez+' !+++!');
            Inc(countDecision);
          end
          else
          begin
            Form1.mmo1.Lines.Add(str1+'+'+str2+'='+rez+'<->'+
            intTostr(str1Num+str2Num)+'='+rez);
          end;
          Inc(s);
        end;
        Inc(q);
      end;
      Inc(t);
    end;
    Inc(r);
  end;

  Form1.edt1.Text:=IntToStr(countDecision);
end;

end.
