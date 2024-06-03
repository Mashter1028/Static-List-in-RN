# Static-List-in-RN
in Static List we can nest on array[ ]  in another array[ ]


import { SectionList, StyleSheet, Text, View } from 'react-native'
import React from 'react'

export default function App() {

  const user=[
    {
      id:1,
      name : 'Saud',
      data:["PHP", "ACCA", "Gurnadier"]
    },

    {
      id:2,
      name :"Ali",
      data:["Camper","Drown","VLC"]
    },
    {
      id:3,
      name:"Rasikh",
      data:["Intellegent", "Elegent"]
    }
  ]
  return (
    <View>
      <Text style={{fontSize:30,}}>Section List in Reach Native</Text>
      <SectionList
      sections={user}
       renderItem={({item})=><Text style={{marginLeft:17,}}>{item}</Text>}
       renderSectionHeader={({section:{name}})=><Text style={{fontSize:20,color:"red"}}>{name}</Text>}
      />
    </View>
  )
}

const styles = StyleSheet.create({})
