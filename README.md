# mydash-expo
cd mydash-expo
import { NavigationContainer } from '@react-navigation/native';
import { StatusBar } from 'expo-status-bar';
import React, {useState} from 'react';
import { StyleSheet, Text, View, Image, TextInput, TouchableOpacity, Button, ScrollView, Alert, Animate, KeyboardAvoidingView, } from 'react-native';

export default function Login({navigation}) {
  
  

  const [email, setEmail] = useState('');
  const [senha, setsenha] = useState('');





 function handleSubmit(){
   alert('Login realizado com sucesso')

   
 }
  
  return (
    <ScrollView>
      <KeyboardAvoidingView
      behavior={Platform.OS === "ios" ? "padding" : "height"} 
      style={{flex:1}}
      >
      

    <View style={styles.container}>
    
      <Text style={styles.titulo}> LOGIN </Text>
      

      <StatusBar style="auto" />

      <Image style={{width:200,height:150, marginBottom: 80,}}source={require('../assets/onibus.jpg')} />

      <TextInput placeholder="Digite seu email.." style={styles.TextInput} value={email} onChangeText={text=>setEmail(text)} />
      <TextInput secureTextEntry={true} placeholder="Digite sua senha.." style={styles.TextInput} value={senha} onChangeText={text=>setsenha(text)} />
      

      <TouchableOpacity 
      style={styles.button}
      onPress={handleSubmit}
      >
        <Text> {styles.buttonText} ENTRAR</Text>


        
      </TouchableOpacity>
      <TouchableOpacity 
      style={styles.button1}
      >
        <Text> {styles.buttonText} CADASTRE</Text>



        
      </TouchableOpacity>
    </View>
    </KeyboardAvoidingView>
    </ScrollView>
  
  );
}

const styles = StyleSheet.create({
  container: { 
    flex: 1,
    backgroundColor: '#2AA9D3',
    alignItems: 'center',
    justifyContent: 'center',
    padding:80
    
    
  },
  TextInput:{
    fontWeight: 'bold',
    marginBottom: 20,
    textAlign: 'center',
    fontSize: 16,
    marginHorizontal: 20,
    borderRadius: 10,
    width: '90%',
    height: 60,
    backgroundColor: 'white'
    
    
  },
  titulo:{
    fontWeight: 'bold',
    margin: 20,
    fontSize: 16,
    padding: 5,
    height: 30,
    backgroundColor: '#BAD739'
    
  },

  button:{
    height:40 ,
    padding: 10,
    fontSize: 16,
    margin: 15,
    fontWeight: 'bold',
    backgroundColor: '#76B82A'
    
    

  },

  button1:{
    height: 40,
    padding: 10,
    fontSize: 16,
    margin: 10,
    fontWeight: 'bold',
    backgroundColor: '#76B82A'

  },




});


