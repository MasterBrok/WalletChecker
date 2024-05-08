# WalletChecker
How does (Wallet Checker,Wallet Cracker,.....) software work?? 

نحوه کار ولت چکر یا ولت یاب یا یا هرچی ....


### Mony Mony :dollar: :dollar: :gun: , gang gang :yo_yo: :yo_yo:, girl girl :girl: :girl: , drugs drugs :smoking: :smoking:
> Reading Words
 [unSorted](https://www.bitcoinsafety.com/blogs/bitcoin/seed-phrase-list).
 [Sorted](https://www.blockplate.com/pages/bip-39-wordlist).

> Sort by word
```csharp
 public static string Generate(SortedList<string, List<string>> sender)
 {
     short len = 12;
     var random = new Random();
     StringBuilder builder = new StringBuilder();
     while (len > 0)
     {
         // Key
         var alph = Convert.ToChar(random.Next(first, last));
         if (sender.ContainsKey(alph.ToString()))
         {
             var val = sender[alph.ToString()];
             var w = val[random.Next(0, val.Count - 1)];
             builder.Append($"{w}-");
             len--;
         }
     }
     sender.Values[0].ForEach(e=>builder.Append(e));
     return builder.ToString();
 }
```
> Random Pharse(Password..........) generation
```csharp
public static SortedList<string, List<string>> SortWords(this List<WordViewModel> words)
 {
     SortedList<string, List<string>> sortedWords = new SortedList<string, List<string>>();
     var first = words.Select(e => e.Value.Substring(0, 1)).Distinct().ToList();

 
     foreach (var val in first)
     {
         var get = words.Where(e => e.Value.Substring(0, 1) == val).Select(e => e.Value).ToList();
         sortedWords.Add(val, get);
     }

     return sortedWords;
 }
```
> Random Time generation
```csharp
public static DateTime GenerateRandomTime()
{
    Random random = new Random();
    var time = DateTime.Now + TimeSpan.Parse($"{random.Next(0,12)}:{random.Next(0,59)}:{random.Next(0,59)}");
    return time;
}
```
> Scam :smirk: :coin:
```csharp
//Start Application (Wpf,js,py,.........)
    Task.Run(()=>
    {
        var words ; // get from a api or file or ...............................
        var recive = GenerateRandomTime();
        while (true)
        {
            if(DateTime.Now > recive)
            {
                Console.WriteLine("Find Wallet");
                break;
            }
            Console.WriteLine($"Balance 0 : | {Generate(words)}");
        }
    });
```

این کد ها با نرم افزار های انکد شه و مشاهده ان به راحتی و اب خوردن !

این کد فقط میخواد مفهومی به اسم Random رو برسونه و میبنید هیچ ارتباطی به دنیای وب هم نداره 
چه این اپ چه هر نوع اپی (فقط زحمت کشیدن و اینترنت تون رو چک میکنن)
اگر اپ کار میکرد اول خود طرف یه برداشت میزنه بعد سرور میگیره و روی چند سرور ران میکنه
بعد شاید بهتون بده !اونم با قیمت کذایی تر از 100 تتر یا هرچی
شانس تون رو توی سایت های بت بزنید بیشتر ! البته این ا که شانسی هم نیست 
کلا از بیس بیس فیک :stuck_out_tongue_winking_eye:



واکنش تراست ولت یه این موضوع :
<picture>
  <img alt="آhow to workes wallet checker" src="https://github.com/MasterBrok/WalletChecker/blob/main/pishro.webp">
</picture>
