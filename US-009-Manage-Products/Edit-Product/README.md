<h1 align=center>

US-009.2-Diagrams & Pseudocode

</h1>

## Flowchart

### High-level visual representation of the process:

<div align=center>

![Flowchart](./flowchart.png)

 </div>

## Sequence Diagram

### Illustrates the step-by-step interaction between actors and the system:

<div align=center>

![Sequence Diagram](./sequence-diagram.png)

 </div>

## Pseudocode

```text
function editProduct(Product:product){
    if(product.price < 0)
        return "Price cannot be less than zero";

    if(product.quantity < 0)
    return "Quantity cannot be less than zero";

    if(isValidImage(product.image))
        return "Invalid image";

    editProduct(product); // DB Call where we also validate product's info

    return "Product udpated successfully";
}

function isValidImage(image){
    if(image.size > 5MP)
        return false;

    if(image.extention != PNG or JPG)
        return false;

    return true;
}
```
