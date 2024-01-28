allproducts <- list(list(name="apple",price=1.5),
list(name="banana",price=2.0),
list(name="orange",price=0.5),
list(name="butter",price=6),
list(name="milk",price=4.5),
list(name="bread",price=3.0),
list(name="biscuit",price=3.5))
cat("name \t price \n")
cat("=============\n")
for (i in allproducts)
{
    cat(sprintf("%s \t %.2f \n",i$name,i$price))
}


shopping<-list()


carttoitem<-list(list(name="banana",quantity=2),
list(name="orange",quantity=3),
list(name="butter",quantity=5),
list(name="milk",quantity=1))

for(item in carttoitem)
{
    product_name=item$name
    qty=item$quantity
    product=NULL
    for(p in allproducts)
    {
        if(product_name==p$name)
        {
        product<-p
        break
        }
    }
    if(!is.null(product))
    {
        cartitem=list(name=product$name,price=product$price,quantity=qty)
        shopping<-append(shopping,list(cartitem))
        }
}
for (i in shopping)
{
    cat(sprintf("%s \t %.2f \t %d \n",i$name,i$price,i$quantity))
}
subtotal<-0
for(i in shopping)
{
    itemtotal=i$price*i$quantity
    subtotal<-subtotal+itemtotal
    cat(sprintf("%s \t %.2f \n",i$name,itemtotal))
}
cat(sprintf("item in cart before tax %.2f\n",subtotal))
tax<-0.08
total<-subtotal+subtotal*tax
cat(sprintf("item in cart after tax %.2f\n",total))
