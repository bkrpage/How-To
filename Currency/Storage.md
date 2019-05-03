# Currency Storage

According to the *Generally Accepted Accounting Principles (GAAP)* - Currency should be storaged in MySQL as a `DECIMAL(13,4)`.

Rationalisation found in the comments of this article: https://rietta.com/blog/2012/03/03/best-data-types-for-currencymoney-in/ from *anne.ominous*:
 
> I learned this back when I was working with money data in the (then relatively new) Microsoft ‘Currency’ type in their ISAM database engine:
>
> If you want to meet Generally Accepted Accounting Principles (GAAP), you need to have at least FOUR decimal places. This ensures that rounding errors will not, on average, exceed $0.01 more often than many thousand transactions (because rounding errors tend to even out).
>
>If, on the other hand, you are only using 2 decimal places, you can expect rounding errors to equal or exceed $0.01 fairly frequently.
>
>Microsoft’s Currency type, by the way, behaves like a 4-decimal-place Decimal type, but is stored in the database as a scaled integer for exactitude.
>
>It is pretty easy to write routines that emulate this behavior. Or as you say, with MySQL you can use Decimal and still get exact storage. But you should use 4 decimal places, not 2.