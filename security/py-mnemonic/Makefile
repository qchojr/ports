# Created by: Emanuel Haupt <ehaupt@FreeBSD.org>

PORTNAME=	mnemonic
PORTVERSION=	0.19
CATEGORIES=	security python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ehaupt@FreeBSD.org
COMMENT=	Implementation of Bitcoin BIP-0039

LICENSE=	MIT

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}pbkdf2>=1.3:security/py-pbkdf2@${PY_FLAVOR}

USES=		python:3.6+
USE_PYTHON=	autoplist distutils

.include <bsd.port.mk>
