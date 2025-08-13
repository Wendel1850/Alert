# Alert
Aqui está um exemplo de como criar um componente de alerta de mensagem em React:

Alert.js
import React from 'react';

const Alert = ({ type, message }) => {
  const classes = type === 'success' ? 'alert-success' : type === 'error' ? 'alert-error' : 'alert-info';

  return (
    <div className={`alert ${classes}`}>
      {message}
    </div>
  );
};

export default Alert;

Estilos CSS
.alert {
  padding: 10px;
  border-radius: 5px;
  font-size: 16px;
  font-weight: bold;
}

.alert-success {
  background-color: #dff0d8;
  border: 1px solid #8bc34a;
  color: #3e8e41;
}

.alert-error {
  background-color: #f2dede;
  border: 1px solid #a94442;
  color: #a94442;
}

.alert-info {
  background-color: #d9edf7;
  border: 1px solid #31708f;
  color: #31708f;
}

Uso do componente
import React from 'react';
import Alert from './Alert';

const App = () => {
  return (
    <div>
      <Alert type="success" message="Operação realizada com sucesso!" />
      <Alert type="error" message="Erro ao realizar a operação!" />
      <Alert type="info" message="Informação importante!" />
    </div>
  );
};

export default App;

Esse exemplo demonstra como criar um componente de alerta de mensagem que pode ser utilizado em diferentes situações, como sucesso, erro ou informação. O componente utiliza classes CSS para estilizar a mensagem de alerta.

Adicionando animação
.alert {
  animation: fadeIn 0.5s;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

Adicionando botão de fechar
import React from 'react';

const Alert = ({ type, message, onClose }) => {
  const classes = type === 'success' ? 'alert-success' : type === 'error' ? 'alert-error' : 'alert-info';

  return (
    <div className={`alert ${classes}`}>
      {message}
      <button className="close" onClick={onClose}>
        ×
      </button>
    </div>
  );
};

export default Alert;

Essas são apenas algumas ideias para melhorar o componente de alerta de mensagem. Você pode personalizar e estender o componente para atender às necessidades específicas do seu aplicativo.
.close {
  position: absolute;
  top: 5px;
  right: 5px;
  font-size: 20px;
  cursor: pointer;
}
