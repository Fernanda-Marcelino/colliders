# Colliders

### Autores
Fernanda e Arthur

## Introdução 
Nosso projeto feito no Unity 3D, a pedido da orientadora Aline Brito.

### Colisores Usados 

 ```Static Collider
 Rigibody Collider 
 Kinematic Collider
 E seus Colliders Triggers```


### O Jogo 
O nosso jogo é feito com o objetivo simples de um sobrevivente, atropelar, com seu kart uma horda de monstros presentes no local.

## Códigos e onde se encontram 

### Carro 
No carro, ou kart se encontra o ```Rigibody Collider``` usado para simularam uma mecânica de física, que reagem ou não a colisões e colocar forças aplicadas ao script


### Monstros 
Os Monstros têm como função apenas serem atropelados e "morrerem", por isso colocamos o ```Kinematic Collider``` que são scripts utilizados para transformar ou não seu item inserido no script, um exemplo é uma porta que você pode abrir ou não, mas mesmo não abrindo ela vai estar lá para caso queira abrir.


### Árvores e pedras 
Não menos importante Usamos nas árvores e pedras o ```Static Collider``` que são usados para colocar uma colisão no objeto parado, pode ser utilizado no chão, parede, objetos não animados e etc.


* Codigo usado para colisão trigger dos monstros 
```ruby 
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class andar : MonoBehaviour
{
    public float velo = 10f;

    void Start()
    {

    }


    void Update()
    {
        float movimentoH = Input.GetAxis("Horizontal"); // A e D ou setas esquerda/direita
        float movimentoV = Input.GetAxis("Vertical"); // W e S ou setas cima/baixo

        Vector3 mover = new Vector3(0, 0, movimentoV) * velo * Time.deltaTime;

        transform.Translate(mover);
        transform.Rotate(0f, movimentoH * 1.2f, 0f);
    }

    private void OnTriggerEnter(Collider other) {
   
   if( other.gameObject.CompareTag("PickUp")){
       
        other.gameObject.SetActive(false);

   } 
}
}
```


# Galeria
* Foto 1
![Captura de tela 2023-10-31 194336](https://github.com/Fernanda-Marcelino/colliders/assets/128320607/33bf4dfe-8709-4a11-bfa2-4439dd50eaa0)
* Foto 2
![Captura de tela 2023-10-31 194317](https://github.com/Fernanda-Marcelino/colliders/assets/128320607/9ce92556-969a-4b70-b508-7f15457127f4)


* Vídeo Do Jogo 



# Link Do Unity
https://drive.google.com/drive/folders/1lf0EU4wNhg207JT9fqUC2BsxgI2Z2je0?usp=sharing