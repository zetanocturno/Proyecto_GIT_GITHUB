\# Esquema GraphQL - API de Sistema de Gestión



\## Definición de Tipos



```graphql

\# Tipo Usuario

type Usuario {

&nbsp; id: ID!

&nbsp; nombre: String!

&nbsp; email: String!

&nbsp; rol: Rol!

&nbsp; fechaRegistro: String

&nbsp; pedidos: \[Pedido]

}



\# Tipo Producto

type Producto {

&nbsp; id: ID!

&nbsp; nombre: String!

&nbsp; descripcion: String

&nbsp; precio: Float!

&nbsp; stock: Int!

&nbsp; categoria: Categoria!

}



\# Tipo Pedido

type Pedido {

&nbsp; id: ID!

&nbsp; usuario: Usuario!

&nbsp; productos: \[ProductoEnPedido!]!

&nbsp; total: Float!

&nbsp; estado: EstadoPedido!

&nbsp; fecha: String!

}



\# Tipos auxiliares

type ProductoEnPedido {

&nbsp; producto: Producto!

&nbsp; cantidad: Int!

}



enum Rol {

&nbsp; ADMIN

&nbsp; USUARIO

&nbsp; INVITADO

}



enum EstadoPedido {

&nbsp; PENDIENTE

&nbsp; ENVIADO

&nbsp; ENTREGADO

&nbsp; CANCELADO

}



input UsuarioInput {

&nbsp; nombre: String!

&nbsp; email: String!

&nbsp; password: String!

}



\# Queries

type Query {

&nbsp; usuario(id: ID!): Usuario

&nbsp; usuarios(limite: Int): \[Usuario!]!

&nbsp; producto(id: ID!): Producto

&nbsp; productos(categoria: String): \[Producto!]!

&nbsp; pedido(id: ID!): Pedido

&nbsp; pedidosPorUsuario(usuarioId: ID!): \[Pedido!]!

}



\# Mutations

type Mutation {

&nbsp; crearUsuario(input: UsuarioInput!): Usuario!

&nbsp; actualizarUsuario(id: ID!, input: UsuarioInput!): Usuario!

&nbsp; eliminarUsuario(id: ID!): Boolean!

&nbsp; crearPedido(usuarioId: ID!, productos: \[ProductoInput!]!): Pedido!

}

