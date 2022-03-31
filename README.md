import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: new ThemeData(scaffoldBackgroundColor: const Color(0xFFEFEFEF)),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  final addNome = TextEditingController ();
  
  @override
  // Designer da tela de login
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.white10,
      body: Padding(
        padding: EdgeInsets.all(10),
        child: Center(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.center,
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              
               const Text(
                'Agenda',
                style: TextStyle(
                fontSize: 24,
                height: 5.0,
                ),
              ),
              
              // Email
              TextFormField(
                autofocus: true,
                keyboardType: TextInputType.text,
                style: new TextStyle(color: Colors.black, fontSize: 20),
                decoration: InputDecoration(
                    border: OutlineInputBorder(),
                    labelText: "Nome:",
                    labelStyle: TextStyle(color: Colors.black)),
              ),
              // nome
              Divider(),
              TextFormField(
                autofocus: true,
                keyboardType: TextInputType.text,
                style: new TextStyle(color: Colors.black, fontSize: 20),
                decoration: InputDecoration(
                    border: OutlineInputBorder(),
                    labelText: "Telefone:",
                    labelStyle: TextStyle(color: Colors.black)),
              ),
              // Senha
              Divider(),
              TextFormField(
                autofocus: true,
                obscureText: true,
                keyboardType: TextInputType.text,
                style: new TextStyle(color: Colors.black, fontSize: 20),
                decoration: InputDecoration(
                    border: OutlineInputBorder(),
                    labelText: "E-mail:",
                    labelStyle: TextStyle(color: Colors.black)),
              ),
              //Botão "Fazer Login"
              Divider(),
              ButtonTheme(
                height: 60.0,
                child: RaisedButton(
                  onPressed: () {},
                  child: Text(
                    "Adicionar",
                    style: TextStyle(color: Colors.white),
                  ),
                  color: Colors.black,
                ),
              ),
              // Botão "Entrar com o logn"
              Divider(),
              ButtonTheme(
                height: 60.0,
                child: RaisedButton(
                  onPressed: () {
                     print(minhaListaNomes.length);
                  },
                  child: Text(
                    'Mostrar',
                    style: TextStyle(color: Colors.white),
                  ),
                  color: Colors.black,
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
